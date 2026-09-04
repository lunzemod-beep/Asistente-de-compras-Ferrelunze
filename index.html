<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FerreLunze - Control de Compras & Análisis de Márgenes</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Supabase SDK -->
    <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
    <!-- FontAwesome Iconos -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;800&display=swap');
        body { font-family: 'Inter', sans-serif; background-color: #f3f4f6; }
    </style>
</head>
<body class="bg-gray-100 min-h-screen text-gray-800">

    <!-- Header Corporativo -->
    <header class="bg-gray-900 text-white shadow-lg border-b-4 border-yellow-500">
        <div class="max-w-7xl mx-auto px-4 py-3 flex justify-between items-center">
            <div class="flex items-center space-x-3">
                <div class="bg-yellow-500 text-gray-900 p-2 rounded-lg font-black text-xl flex items-center justify-center w-10 h-10 shadow">
                    <i class="fa-solid fa-chart-line"></i>
                </div>
                <div>
                    <h1 class="text-xl font-extrabold tracking-wider text-yellow-500 leading-none">FERRELUNZE</h1>
                    <p class="text-xs text-gray-400 font-medium">Control Estratégico de Compras & Márgenes</p>
                </div>
            </div>
            <span class="bg-gray-800 text-yellow-400 text-xs font-semibold px-3 py-1.5 rounded-full border border-yellow-500/30 flex items-center gap-2">
                <span class="w-2 h-2 rounded-full bg-green-500 animate-pulse"></span> Sistema Analítico Activo
            </span>
        </div>
    </header>

    <main class="max-w-7xl mx-auto p-4 md:p-6 space-y-6">

        <!-- TARJETAS DE MÉTRICAS DE NEGOCIO (KPIs) -->
        <section class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
            <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                <div class="flex justify-between items-center text-gray-500 text-xs font-bold uppercase mb-1">
                    <span>Total Comprado ($)</span>
                    <i class="fa-solid fa-cart-shopping text-yellow-600 text-base"></i>
                </div>
                <div id="kpi-total-compras" class="text-2xl font-black text-gray-900">$0</div>
                <span class="text-[10px] text-gray-400">Inversión acumulada en inventario</span>
            </div>

            <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                <div class="flex justify-between items-center text-gray-500 text-xs font-bold uppercase mb-1">
                    <span>Ítems Analizados</span>
                    <i class="fa-solid fa-boxes-stacked text-blue-600 text-base"></i>
                </div>
                <div id="kpi-num-items" class="text-2xl font-black text-gray-900">0</div>
                <span class="text-[10px] text-gray-400">Productos ingresados</span>
            </div>

            <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                <div class="flex justify-between text-xs font-bold uppercase mb-1">
                    <span class="text-gray-500">Margen Promedio</span>
                    <i class="fa-solid fa-percent text-green-600 text-base"></i>
                </div>
                <div id="kpi-margen-promedio" class="text-2xl font-black text-green-600">0%</div>
                <span class="text-[10px] text-gray-400">Rentabilidad estimada FerreLunze</span>
            </div>

            <div class="bg-white p-5 rounded-xl shadow-sm border border-gray-200">
                <div class="flex justify-between text-xs font-bold uppercase mb-1">
                    <span class="text-gray-500">Alertas de Bajo Margen</span>
                    <i class="fa-solid fa-triangle-exclamation text-red-500 text-base"></i>
                </div>
                <div id="kpi-alertas" class="text-2xl font-black text-red-600">0</div>
                <span class="text-[10px] text-red-500 font-semibold">Productos con margen &lt; 20%</span>
            </div>
        </section>

        <!-- FORMULARIO DE INGRESO CON CÁLCULO DE MÁRGENES -->
        <section class="bg-white rounded-xl shadow-md border border-gray-200 overflow-hidden">
            <div class="bg-gray-50 px-6 py-4 border-b border-gray-200 flex justify-between items-center">
                <h2 class="text-base font-bold text-gray-800 flex items-center gap-2">
                    <i class="fa-solid fa-plus-circle text-yellow-600"></i> Registrar Factura & Auditar Costos
                </h2>
            </div>

            <form id="analitic-form" class="p-6 space-y-6">
                <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
                    <div>
                        <label class="block text-xs font-bold text-gray-700 uppercase mb-1">NIT Proveedor *</label>
                        <input type="text" id="prov-nit" required placeholder="Ej: 900123456-1" class="w-full border border-gray-300 rounded-lg p-2.5 text-sm font-medium focus:ring-2 focus:ring-yellow-500 focus:outline-none">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Razón Social *</label>
                        <input type="text" id="prov-name" required placeholder="Ej: Tornicenter / REDDI" class="w-full border border-gray-300 rounded-lg p-2.5 text-sm font-medium focus:ring-2 focus:ring-yellow-500 focus:outline-none">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-gray-700 uppercase mb-1">N° Factura *</label>
                        <input type="text" id="doc-number" required placeholder="FE-9982" class="w-full border border-gray-300 rounded-lg p-2.5 text-sm font-medium focus:ring-2 focus:ring-yellow-500 focus:outline-none">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Fecha Emisión *</label>
                        <input type="date" id="doc-date" required class="w-full border border-gray-300 rounded-lg p-2.5 text-sm font-medium focus:ring-2 focus:ring-yellow-500 focus:outline-none">
                    </div>
                </div>

                <div>
                    <div class="flex justify-between items-center mb-2">
                        <h3 class="text-xs font-bold text-gray-700 uppercase">Productos & Control de Márgenes</h3>
                        <button type="button" id="add-row-btn" class="text-xs bg-yellow-500 hover:bg-yellow-600 text-gray-900 font-bold px-3 py-1.5 rounded-lg transition">
                            <i class="fa-solid fa-plus mr-1"></i> Añadir Ítem
                        </button>
                    </div>

                    <div class="overflow-x-auto border border-gray-200 rounded-lg">
                        <table class="w-full text-left text-xs">
                            <thead class="bg-gray-100 text-gray-700 font-bold border-b border-gray-200">
                                <tr>
                                    <th class="p-2.5">Código (Opcional)</th>
                                    <th class="p-2.5">Descripción Producto *</th>
                                    <th class="p-2.5 w-20 text-center">Cant. *</th>
                                    <th class="p-2.5 w-28 text-right">Costo Unit. ($) *</th>
                                    <th class="p-2.5 w-28 text-right bg-yellow-50">Precio Venta ($) *</th>
                                    <th class="p-2.5 w-24 text-center">Margen (%)</th>
                                    <th class="p-2.5 w-28 text-right">Subtotal ($)</th>
                                    <th class="p-2.5 w-10 text-center"></th>
                                </tr>
                            </thead>
                            <tbody id="items-body" class="divide-y divide-gray-200 bg-white">
                            </tbody>
                        </table>
                    </div>
                </div>

                <div class="flex flex-col md:flex-row justify-between items-center gap-4 bg-gray-50 p-4 rounded-lg border border-gray-200">
                    <div class="text-xs text-gray-500">
                        <i class="fa-solid fa-circle-info text-blue-500"></i> El sistema compara el costo actual contra compras anteriores para alertar si el proveedor subió el precio.
                    </div>
                    <div class="flex items-center gap-6">
                        <div class="text-right">
                            <span class="block text-xs text-gray-500 font-bold uppercase">Total Factura:</span>
                            <span id="grand-total-display" class="text-xl font-black text-yellow-600">$0</span>
                        </div>
                        <button type="submit" id="save-btn" class="bg-green-600 hover:bg-green-700 text-white font-bold py-3 px-6 rounded-lg shadow-md transition flex items-center gap-2">
                            <i class="fa-solid fa-floppy-disk"></i> Registrar & Analizar
                        </button>
                    </div>
                </div>
            </form>
        </section>

        <!-- MÓDULO DE ANÁLISIS Y SEGUIMIENTO DE VARIACIÓN DE PRECIOS -->
        <section class="bg-white rounded-xl shadow-md border border-gray-200 overflow-hidden">
            <div class="bg-gray-50 px-6 py-4 border-b border-gray-200 flex justify-between items-center">
                <h2 class="text-base font-bold text-gray-800 flex items-center gap-2">
                    <i class="fa-solid fa-magnifying-glass-dollar text-yellow-600"></i> Auditoría de Precios, Variaciones & Rentabilidad
                </h2>
                <button id="refresh-btn" class="text-xs text-gray-600 hover:text-gray-900 font-semibold">
                    <i class="fa-solid fa-rotate mr-1"></i> Actualizar Tabla
                </button>
            </div>

            <div class="overflow-x-auto">
                <table class="w-full text-left text-xs">
                    <thead class="bg-gray-100 text-gray-700 font-bold border-b border-gray-200">
                        <tr>
                            <th class="p-3">Fecha</th>
                            <th class="p-3">Proveedor</th>
                            <th class="p-3">Producto</th>
                            <th class="p-3 text-center">Cant.</th>
                            <th class="p-3 text-right">Costo Actual</th>
                            <th class="p-3 text-right">Costo Anterior</th>
                            <th class="p-3 text-center">Variación %</th>
                            <th class="p-3 text-right">Precio Venta</th>
                            <th class="p-3 text-right">Ganancia ($)</th>
                            <th class="p-3 text-center">Margen (%)</th>
                        </tr>
                    </thead>
                    <tbody id="analysis-body" class="divide-y divide-gray-200">
                        <tr>
                            <td colspan="10" class="p-4 text-center text-gray-400">Cargando datos de rendimiento...</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

    </main>

    <script>
        const SUPABASE_URL = "https://quwbispzyxjgdgreyfrt.supabase.co";
        const SUPABASE_KEY = "sb_publishable_60xint6SFkAVBMxG6soK5A_VrZOq832_";
        const supabase = window.supabase.createClient(SUPABASE_URL, SUPABASE_KEY);

        const itemsBody = document.getElementById('items-body');
        const addRowBtn = document.getElementById('add-row-btn');
        const analiticForm = document.getElementById('analitic-form');
        const grandTotalDisplay = document.getElementById('grand-total-display');
        const analysisBody = document.getElementById('analysis-body');

        document.getElementById('doc-date').value = new Date().toISOString().split('T')[0];

        function agregarFila(code = '', desc = '', qty = 1, cost = 0, price = 0) {
            const tr = document.createElement('tr');
            tr.className = 'hover:bg-gray-50';
            tr.innerHTML = `
                <td class="p-2"><input type="text" class="item-code w-full border border-gray-300 rounded p-1 text-xs" placeholder="Cód." value="${code}"></td>
                <td class="p-2"><input type="text" required class="item-desc w-full border border-gray-300 rounded p-1 text-xs" placeholder="Ej: Disco Corte 4 1/2" value="${desc}"></td>
                <td class="p-2"><input type="number" required step="0.01" min="0.01" class="item-qty w-full border border-gray-300 rounded p-1 text-xs text-center" value="${qty}"></td>
                <td class="p-2"><input type="number" required step="0.01" min="0" class="item-cost w-full border border-gray-300 rounded p-1 text-xs text-right" value="${cost}"></td>
                <td class="p-2 bg-yellow-50/50"><input type="number" required step="0.01" min="0" class="item-price w-full border border-yellow-300 rounded p-1 text-xs text-right font-bold text-gray-800" value="${price}"></td>
                <td class="p-2 text-center"><span class="item-margin font-bold px-2 py-0.5 rounded text-[11px]">0%</span></td>
                <td class="p-2"><input type="text" readonly class="item-subtotal w-full border border-gray-200 bg-gray-50 rounded p-1 text-xs text-right font-bold text-gray-700" value="$0"></td>
                <td class="p-2 text-center">
                    <button type="button" class="delete-btn text-red-500 hover:text-red-700"><i class="fa-solid fa-trash-can"></i></button>
                </td>
            `;

            itemsBody.appendChild(tr);

            const qtyInput = tr.querySelector('.item-qty');
            const costInput = tr.querySelector('.item-cost');
            const priceInput = tr.querySelector('.item-price');
            const marginBadge = tr.querySelector('.item-margin');
            const subtotalInput = tr.querySelector('.item-subtotal');

            const calcularValores = () => {
                const q = parseFloat(qtyInput.value) || 0;
                const c = parseFloat(costInput.value) || 0;
                const p = parseFloat(priceInput.value) || 0;

                const subtotal = q * c;
                subtotalInput.value = '$' + subtotal.toLocaleString();

                let pct = 0;
                if (p > 0) {
                    pct = ((p - c) / p) * 100;
                }

                marginBadge.innerText = pct.toFixed(1) + '%';

                if (pct < 20) {
                    marginBadge.className = "item-margin font-bold px-2 py-0.5 rounded text-[11px] bg-red-100 text-red-700";
                } else if (pct >= 20 && pct < 35) {
                    marginBadge.className = "item-margin font-bold px-2 py-0.5 rounded text-[11px] bg-yellow-100 text-yellow-800";
                } else {
                    marginBadge.className = "item-margin font-bold px-2 py-0.5 rounded text-[11px] bg-green-100 text-green-800";
                }

                recalcularTotalGeneral();
            };

            qtyInput.addEventListener('input', calcularValores);
            costInput.addEventListener('input', calcularValores);
            priceInput.addEventListener('input', calcularValores);

            tr.querySelector('.delete-btn').addEventListener('click', () => {
                tr.remove();
                recalcularTotalGeneral();
            });

            calcularValores();
        }

        function recalcularTotalGeneral() {
            let total = 0;
            document.querySelectorAll('#items-body tr').forEach(tr => {
                const q = parseFloat(tr.querySelector('.item-qty').value) || 0;
                const c = parseFloat(tr.querySelector('.item-cost').value) || 0;
                total += (q * c);
            });
            grandTotalDisplay.innerText = '$' + total.toLocaleString();
            return total;
        }

        agregarFila();
        addRowBtn.addEventListener('click', () => agregarFila());

        // Guardar Factura con Análisis en Supabase
        analiticForm.addEventListener('submit', async (e) => {
            e.preventDefault();
            const saveBtn = document.getElementById('save-btn');
            saveBtn.disabled = true;
            saveBtn.innerHTML = '<i class="fa-solid fa-spinner fa-spin"></i> Procesando...';

            try {
                const nit = document.getElementById('prov-nit').value.trim();
                const razonSocial = document.getElementById('prov-name').value.trim();
                const numFactura = document.getElementById('doc-number').value.trim();
                const fecha = document.getElementById('doc-date').value;
                const totalFactura = recalcularTotalGeneral();

                // 1. Obtener o crear proveedor
                let { data: prov } = await supabase.from('proveedores').select('id').eq('nit', nit).maybeSingle();

                if (!prov) {
                    const { data: newProv, error: errProv } = await supabase.from('proveedores').insert([{ nit: nit, razon_social: razonSocial }]).select().single();
                    if (errProv) throw errProv;
                    prov = newProv;
                }

                // 2. Insertar Cabecera de Factura
                const { data: factura, error: errFactura } = await supabase.from('facturas_compra').insert([{
                    proveedor_id: prov.id,
                    numero_factura: numFactura,
                    fecha_emision: fecha,
                    subtotal: totalFactura,
                    total_factura: totalFactura
                }]).select().single();

                if (errFactura) throw errFactura;

                // 3. Insertar Detalle con Precios de Venta
                const detalles = [];
                document.querySelectorAll('#items-body tr').forEach(tr => {
                    const code = tr.querySelector('.item-code').value.trim();
                    const desc = tr.querySelector('.item-desc').value.trim();
                    const qty = parseFloat(tr.querySelector('.item-qty').value) || 0;
                    const cost = parseFloat(tr.querySelector('.item-cost').value) || 0;
                    const price = parseFloat(tr.querySelector('.item-price').value) || 0;

                    detalles.push({
                        factura_id: factura.id,
                        codigo_producto: code,
                        descripcion: desc,
                        cantidad: qty,
                        precio_unitario: cost,
                        precio_venta_publico: price,
                        subtotal_linea: qty * cost
                    });
                });

                const { error: errDetalle } = await supabase.from('detalle_compra').insert(detalles);
                if (errDetalle) throw errDetalle;

                alert('¡Factura ' + numFactura + ' registrada y analizada con éxito!');
                analiticForm.reset();
                itemsBody.innerHTML = '';
                agregarFila();
                cargarAnalisis();

            } catch (err) {
                console.error(err);
                alert('Error al guardar: ' + (err.message || 'Verifica la conexión.'));
            } finally {
                saveBtn.disabled = false;
                saveBtn.innerHTML = '<i class="fa-solid fa-floppy-disk"></i> Registrar & Analizar';
            }
        });

        // Cargar Auditoría y Métricas del Sistema
        async function cargarAnalisis() {
            analysisBody.innerHTML = '<tr><td colspan="10" class="p-4 text-center text-gray-400">Cargando métricas...</td></tr>';

            const { data, error } = await supabase
                .from('vista_analisis_costos')
                .select('*')
                .order('fecha_emision', { ascending: false })
                .limit(20);

            if (error || !data || data.length === 0) {
                analysisBody.innerHTML = '<tr><td colspan="10" class="p-4 text-center text-gray-400">Sin datos registrados aún. Ingresa tu primera factura arriba.</td></tr>';
                return;
            }

            analysisBody.innerHTML = '';
            let sumaMargen = 0;
            let totalInversion = 0;
            let alertasBajoMargen = 0;

            data.forEach(item => {
                const ganancia = item.utilidad_bruta || 0;
                const margen = item.porcentaje_margen || 0;
                const variacion = item.variacion_porcentaje || 0;
                
                sumaMargen += margen;
                totalInversion += (item.costo_actual * item.cantidad);

                if (margen < 20) alertasBajoMargen++;

                let varBadge = `<span class="text-gray-400">0%</span>`;
                if (variacion > 0) {
                    varBadge = `<span class="bg-red-100 text-red-800 px-1.5 py-0.5 rounded font-bold"><i class="fa-solid fa-arrow-up text-[9px]"></i> +${variacion}%</span>`;
                } else if (variacion < 0) {
                    varBadge = `<span class="bg-green-100 text-green-800 px-1.5 py-0.5 rounded font-bold"><i class="fa-solid fa-arrow-down text-[9px]"></i> ${variacion}%</span>`;
                }

                const tr = document.createElement('tr');
                tr.className = 'hover:bg-gray-50';
                tr.innerHTML = `
                    <td class="p-3 text-gray-500">${item.fecha_emision}</td>
                    <td class="p-3 font-medium text-gray-800">${item.proveedor}</td>
                    <td class="p-3 font-bold text-gray-900">${item.descripcion}</td>
                    <td class="p-3 text-center">${item.cantidad}</td>
                    <td class="p-3 text-right font-mono">$${parseFloat(item.costo_actual).toLocaleString()}</td>
                    <td class="p-3 text-right font-mono text-gray-400">$${parseFloat(item.costo_anterior).toLocaleString()}</td>
                    <td class="p-3 text-center">${varBadge}</td>
                    <td class="p-3 text-right font-mono text-gray-700">$${parseFloat(item.precio_venta_publico).toLocaleString()}</td>
                    <td class="p-3 text-right font-mono font-bold text-green-600">$${parseFloat(ganancia).toLocaleString()}</td>
                    <td class="p-3 text-center">
                        <span class="px-2 py-0.5 rounded text-[10px] font-bold ${margen < 20 ? 'bg-red-100 text-red-800' : 'bg-green-100 text-green-800'}">
                            ${margen}%
                        </span>
                    </td>
                `;
                analysisBody.appendChild(tr);
            });

            document.getElementById('kpi-total-compras').innerText = '$' + totalInversion.toLocaleString();
            document.getElementById('kpi-num-items').innerText = data.length;
            document.getElementById('kpi-margen-promedio').innerText = (sumaMargen / data.length).toFixed(1) + '%';
            document.getElementById('kpi-alertas').innerText = alertasBajoMargen;
        }

        document.getElementById('refresh-btn').addEventListener('click', cargarAnalisis);
        cargarAnalisis();
    </script>
</body>
</html>
