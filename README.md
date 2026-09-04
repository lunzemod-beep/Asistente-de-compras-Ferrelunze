-- 1. AGREGAR COLUMNA DE PRECIO DE VENTA PÚBLICO AL DETALLE (SI NO EXISTE)
ALTER TABLE detalle_compra 
ADD COLUMN IF NOT EXISTS precio_venta_publico NUMERIC(12, 2) DEFAULT 0.00;

-- 2. VISTA DE ANÁLISIS DE MÁRGENES Y VARIACIÓN DE COSTOS
CREATE OR REPLACE VIEW vista_analisis_costos AS
SELECT 
    d.id AS detalle_id,
    f.fecha_emision,
    p.razon_social AS proveedor,
    d.codigo_producto,
    d.descripcion,
    d.cantidad,
    d.precio_unitario AS costo_actual,
    d.precio_venta_publico,
    -- Margen Bruto ($)
    (d.precio_venta_publico - d.precio_unitario) AS utilidad_bruta,
    -- Margen de Ganancia (%)
    CASE 
        WHEN d.precio_venta_publico > 0 
        THEN ROUND(((d.precio_venta_publico - d.precio_unitario) / d.precio_venta_publico) * 100, 2)
        ELSE 0 
    END AS porcentaje_margen
FROM detalle_compra d
JOIN facturas_compra f ON d.factura_id = f.id
JOIN proveedores p ON f.proveedor_id = p.id;
