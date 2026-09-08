<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Diagnóstico HVAC/R V2</title>
<style>
:root{--bg:#f4f7fa;--card:#fff;--text:#17202a;--muted:#667085;--line:#dbe2ea;--accent:#1769aa;--ok:#198754;--warn:#d97706;--danger:#c62828}
*{box-sizing:border-box}body{margin:0;font-family:Arial,Helvetica,sans-serif;background:var(--bg);color:var(--text)}
header{background:#102a43;color:#fff;padding:22px 28px;position:sticky;top:0;z-index:5}
header h1{margin:0 0 5px;font-size:24px}header p{margin:0;color:#c9d7e5}
main{max-width:1250px;margin:22px auto;padding:0 16px}
.card{background:var(--card);border:1px solid var(--line);border-radius:12px;padding:20px;margin-bottom:18px;box-shadow:0 2px 8px #0000000a}
h2{font-size:18px;margin:0 0 16px}h3{font-size:15px;margin:18px 0 10px}
.grid{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}
.field{display:flex;flex-direction:column;gap:6px}.field label{font-size:13px;font-weight:700}
input,select,textarea{width:100%;padding:10px;border:1px solid #cbd5df;border-radius:8px;font-size:14px;background:#fff}
textarea{min-height:90px;resize:vertical}.unit{display:flex}.unit input{border-radius:8px 0 0 8px}.unit select{width:95px;border-radius:0 8px 8px 0}
.actions{display:flex;gap:10px;flex-wrap:wrap}.btn{border:0;border-radius:8px;padding:11px 16px;font-weight:700;cursor:pointer}.primary{background:var(--accent);color:#fff}.secondary{background:#e9eef4;color:#203040}
.status{display:flex;align-items:center;justify-content:space-between;gap:20px}.badge{padding:9px 14px;border-radius:999px;font-weight:800;font-size:13px}.normal{background:#d9f2e3;color:#12643b}.attention{background:#fff0cf;color:#8a5000}.review{background:#ffe2b8;color:#7a3e00}.critical{background:#ffd7d7;color:#8b1717}.error{background:#e4e7eb;color:#374151}
.results{display:grid;grid-template-columns:repeat(4,1fr);gap:12px}.metric{border:1px solid var(--line);border-radius:10px;padding:14px;background:#fafcfe}.metric .name{font-size:12px;color:var(--muted)}.metric .value{font-size:21px;font-weight:800;margin-top:5px}
.alert{padding:14px;border-left:5px solid var(--warn);background:#fff8eb;border-radius:6px;margin:8px 0}.danger{border-left-color:var(--danger);background:#fff0f0}.ok{border-left-color:var(--ok);background:#effaf3}
ul{margin:8px 0 0 20px;padding:0}li{margin:5px 0}.small{font-size:12px;color:var(--muted)}.hidden{display:none}
footer{text-align:center;color:var(--muted);font-size:12px;padding:15px}
@media(max-width:900px){.grid,.results{grid-template-columns:repeat(2,1fr)}}@media(max-width:600px){.grid,.results{grid-template-columns:1fr}header{position:static}}
</style>
</head>
<body>
<header>
<h1>DIAGNÓSTICO HVAC/R — Asistente de diagnóstico de campo V2</h1>
<p>Mediciones de campo → cálculos → patrón de diagnóstico → siguiente comprobación</p>
</header>

<main>
<section class="card">
<div class="status">
<div><h2 style="margin-bottom:4px">Estado del diagnóstico</h2><span id="statusText">Ingrese las mediciones disponibles.</span></div>
<span id="statusBadge" class="badge error">DATOS INSUFICIENTES</span>
</div>
</section>

<section class="card">
<h2>1. Equipo</h2>
<div class="grid">
<div class="field"><label>Marca</label><input id="brand" placeholder="Ej. Carrier"></div>
<div class="field"><label>Modelo</label><input id="model" placeholder="Modelo"></div>
<div class="field"><label>Tipo de equipo</label><select id="type"><option>Split</option><option>Mini Split</option><option>Unidad paquete</option><option>Refrigeración comercial</option><option>Cámara frigorífica</option><option>Chiller</option><option>Congelación</option><option>Otro</option></select></div>
<div class="field"><label>Refrigerante</label><select id="ref"><option value="R410A">R-410A</option><option value="R32">R-32</option><option value="R134a">R-134a</option><option value="R404A">R-404A</option><option value="R407C">R-407C</option><option value="R22">R-22</option></select></div>
<div class="field"><label>Capacidad</label><input id="capacity" placeholder="Ej. 12000 BTU/h"></div>
<div class="field"><label>Compresor</label><select id="compressor"><option>No identificado</option><option>Scroll</option><option>Reciprocante</option><option>Rotativo</option><option>Tornillo</option><option>Otro</option></select></div>
<div class="field"><label>Fases</label><select id="phases"><option value="1">1Φ</option><option value="3">3Φ</option></select></div>
<div class="field"><label>Frecuencia</label><input id="freq" type="number" placeholder="Hz"></div>
</div>
</section>

<section class="card">
<h2>2. Condiciones de operación</h2>
<div class="grid">
<div class="field"><label>Temperatura ambiente °C</label><input id="tamb" type="number" step="0.1"></div>
<div class="field"><label>Temperatura retorno °C</label><input id="treturn" type="number" step="0.1"></div>
<div class="field"><label>Temperatura suministro °C</label><input id="tsupply" type="number" step="0.1"></div>
<div class="field"><label>Fuente de ambiente</label><select id="ambientSource"><option>Medición de campo</option><option>Dato manual / clima</option></select></div>
</div>
</section>

<section class="card">
<h2>3. Mediciones de refrigeración</h2>
<p class="small">Introduzca únicamente lo que realmente midió. La aplicación no sustituye valores faltantes por valores predeterminados.</p>
<h3>Presiones</h3>
<div class="grid">
<div class="field"><label>Presión de succión</label><div class="unit"><input id="psuc" type="number" step="0.1"><select id="punit"><option value="psi">PSI</option><option value="bar">bar</option><option value="kpa">kPa</option></select></div></div>
<div class="field"><label>Presión de descarga</label><div class="unit"><input id="pdis" type="number" step="0.1"><select id="punit2"><option value="psi">PSI</option><option value="bar">bar</option><option value="kpa">kPa</option></select></div></div>
</div>
<h3>Temperaturas</h3>
<div class="grid">
<div class="field"><label>T° salida evaporador °C</label><input id="tevapout" type="number" step="0.1"></div>
<div class="field"><label>T° succión en compresor °C</label><input id="tsuction" type="number" step="0.1"></div>
<div class="field"><label>T° línea líquida °C</label><input id="tliquid" type="number" step="0.1"></div>
<div class="field"><label>T° descarga compresor °C</label><input id="tdischarge" type="number" step="0.1"></div>
</div>
</section>

<section class="card">
<h2>4. Mediciones eléctricas</h2>
<div class="grid">
<div class="field"><label>Voltaje medido V</label><input id="vmeas" type="number" step="0.1"></div>
<div class="field"><label>Voltaje nominal V</label><input id="vnom" type="number" step="0.1"></div>
<div class="field"><label>Corriente medida A</label><input id="ameas" type="number" step="0.1"></div>
<div class="field"><label>Corriente nominal A</label><input id="anom" type="number" step="0.1"></div>
</div>
<p class="small">La aplicación compara V y A con los datos nominales. No presenta V×A como kW real porque eso requeriría conocer el factor de potencia y, según el caso, la eficiencia.</p>
</section>

<section class="card">
<h2>5. Resultados calculados</h2>
<div id="metrics" class="results"></div>
</section>

<section class="card">
<h2>6. Diagnóstico</h2>
<div id="findings"><div class="alert">Aún no hay suficientes mediciones para emitir un patrón.</div></div>
<h3>Posibles causas</h3><ul id="causes"><li>Se mostrarán cuando exista un patrón compatible.</li></ul>
<h3>REVISAR AHORA</h3>
<div id="next"><div class="alert">Complete las mediciones disponibles y ejecute el diagnóstico.</div></div>
</section>

<section class="card">
<h2>7. Observaciones del técnico</h2>
<textarea id="notes" placeholder="Condición del equipo, ruido, hielo, ventiladores, suciedad, historial, etc."></textarea>
<div class="actions" style="margin-top:12px">
<button class="btn primary" onclick="diagnose()">ACTUALIZAR DIAGNÓSTICO</button>
<button class="btn secondary" onclick="window.print()">IMPRIMIR / GUARDAR PDF</button>
<button class="btn secondary" onclick="saveData()">GUARDAR DATOS</button>
<button class="btn secondary" onclick="loadData()">CARGAR DATOS</button>
<button class="btn secondary" onclick="clearData()">LIMPIAR</button>
</div>
</section>
</main>
<footer>Herramienta de apoyo al diagnóstico. Las conclusiones son patrones compatibles y deben verificarse con mediciones y procedimientos del fabricante.</footer>

<script>
const SAT = {
  R410A:{evap:[[-20,2.0],[-10,3.0],[0,4.8],[5,5.9],[10,7.0],[15,8.2]],cond:[[30,17.8],[40,23.5],[45,26.5],[50,30.0],[55,33.8]]},
  R32:{evap:[[-20,2.0],[-10,3.0],[0,5.0],[5,6.1],[10,7.2],[15,8.5]],cond:[[30,18.2],[40,23.8],[45,27.0],[50,30.6],[55,34.5]]},
  R134a:{evap:[[-20,0.8],[-10,1.5],[0,2.9],[5,3.5],[10,4.1],[15,4.9]],cond:[[30,6.9],[40,10.2],[45,11.8],[50,13.5],[55,15.2]]},
  R404A:{evap:[[-20,2.1],[-10,3.2],[0,4.9],[5,5.9],[10,7.0],[15,8.2]],cond:[[30,13.2],[40,17.7],[45,20.1],[50,22.7],[55,25.4]]},
  R407C:{evap:[[-20,1.8],[-10,2.8],[0,4.5],[5,5.5],[10,6.5],[15,7.7]],cond:[[30,12.0],[40,16.8],[45,19.2],[50,21.7],[55,24.5]]},
  R22:{evap:[[-20,2.5],[-10,3.5],[0,4.9],[5,5.8],[10,6.8],[15,7.9]],cond:[[30,10.5],[40,14.3],[45,16.4],[50,18.6],[55,20.9]]}
};

function num(id){const v=parseFloat(document.getElementById(id).value);return Number.isFinite(v)?v:null}
function interp(points,p){
  if(p===null||!points) return null;
  if(p<=points[0][1]) return points[0][0];
  if(p>=points.at(-1)[1]) return points.at(-1)[0];
  for(let i=0;i<points.length-1;i++){
    const [t1,p1]=points[i],[t2,p2]=points[i+1];
    if(p>=p1&&p<=p2)return t1+(p-p1)*(t2-t1)/(p2-p1);
  } return null;
}
function pressureBar(v,u){
  if(v===null)return null;
  if(u==='psi')return v*0.0689476;
  if(u==='kpa')return v/100;
  return v;
}
function val(id){return document.getElementById(id).value}
function setStatus(cls,text,sub){
  const b=document.getElementById('statusBadge');b.className='badge '+cls;b.textContent=text;
  document.getElementById('statusText').textContent=sub;
}
function metric(name,value,unit=''){
  return `<div class="metric"><div class="name">${name}</div><div class="value">${value===null?'—':value+unit}</div></div>`;
}
function diagnose(){
  const ref=val('ref'), data=SAT[ref];
  const tamb=num('tamb'), tr=num('treturn'), ts=num('tsupply');
  const ps=pressureBar(num('psuc'),val('punit')), pd=pressureBar(num('pdis'),val('punit2'));
  const teo=num('tevapout'), tsuc=num('tsuction'), tliq=num('tliquid'), tdis=num('tdischarge');
  const vm=num('vmeas'), vn=num('vnom'), am=num('ameas'), an=num('anom');

  const tev=interp(data.evap,ps), tcond=interp(data.cond,pd);
  const shEv=(teo!==null&&tev!==null)?teo-tev:null;
  const shTot=(tsuc!==null&&tev!==null)?tsuc-tev:null;
  const sc=(tliq!==null&&tcond!==null)?tcond-tliq:null;
  const dtAir=(tr!==null&&ts!==null)?tr-ts:null;
  const dtCond=(tcond!==null&&tamb!==null)?tcond-tamb:null;
  const ratio=(ps!==null&&pd!==null&&ps>0)?(pd+1.01325)/(ps+1.01325):null;
  const vDev=(vm!==null&&vn&&vn>0)?(vm-vn)/vn*100:null;
  const iPct=(am!==null&&an&&an>0)?am/an*100:null;

  document.getElementById('metrics').innerHTML=[
    metric('T° saturación evaporación',tev?.toFixed(1),' °C'),
    metric('T° saturación condensación',tcond?.toFixed(1),' °C'),
    metric('Superheat evaporador',shEv?.toFixed(1),' K'),
    metric('Superheat total',shTot?.toFixed(1),' K'),
    metric('Subcooling',sc?.toFixed(1),' K'),
    metric('ΔT aire retorno-suministro',dtAir?.toFixed(1),' K'),
    metric('ΔT condensación-ambiente',dtCond?.toFixed(1),' K'),
    metric('Relación de presión',ratio?.toFixed(2),''),
    metric('Desvío de voltaje',vDev?.toFixed(1),' %'),
    metric('Corriente vs nominal',iPct?.toFixed(1),' %')
  ].join('');

  const haveRef=ps!==null&&pd!==null, haveTemps=tev!==null&&tcond!==null;
  if((ps!==null&&ps<=0)||(pd!==null&&pd<=0)||((vm!==null&&vm<=0))||((am!==null&&am<0))){
    setStatus('error','ERROR DE DATOS','Revise presiones, voltaje y corriente: hay valores físicamente inválidos.');
    document.getElementById('findings').innerHTML='<div class="alert danger">No se modifica ni corrige automáticamente ningún valor ingresado.</div>';
    return;
  }
  if(!haveRef){
    setStatus('error','DATOS INSUFICIENTES','Se necesitan al menos presión de succión y descarga para calcular saturaciones.');
    renderDefault();
    return;
  }
  if(tev===null||tcond===null){
    setStatus('error','FUERA DE RANGO','La presión ingresada queda fuera de la tabla simplificada disponible para este refrigerante.');
    document.getElementById('findings').innerHTML='<div class="alert danger">No extrapole esta tabla. Use la tabla/PT del refrigerante y rango de operación correspondiente.</div>';
    return;
  }

  const findings=[], causes=new Set(), next=[];
  const add=(title,detail,cs,ns,level='attention')=>{
    findings.push({title,detail,level});(cs||[]).forEach(x=>causes.add(x));(ns||[]).forEach(x=>next.push(x));
  };

  // Validaciones de coherencia
  if(shTot!==null&&shEv!==null&&shTot<shEv-1.5)
    add('Revisar ubicación de temperaturas','El superheat total resulta menor que el superheat medido a la salida del evaporador. Verifique puntos de medición y estabilidad.',[],['Confirmar ubicación de T° salida evaporador y T° succión.'],'review');

  if(sc!==null&&sc<0)
    add('Sin subcooling / posible condición anómala','La temperatura de líquido está por encima de la saturación de condensación calculada.',[
      'Carga insuficiente','Presencia de gas en línea líquida','Problema de medición'
    ],['Verificar ubicación de T° línea líquida y presión de descarga.'],'review');

  // Patrón: bajo SH
  if(shEv!==null&&shEv<3){
    add('Superheat evaporador bajo','Patrón compatible con sobrealimentación del evaporador y posible riesgo de retorno de líquido si la condición persiste.',[
      'Válvula de expansión/TXV/EEV sobrealimentando','Control de expansión incorrecto','Carga excesiva o condición de operación particular'
    ],['Verificar superheat estable y control de expansión.','Confirmar que no exista retorno de líquido al compresor.'],'critical');
  }

  // Patrón: evaporador subalimentado
  if(shEv!==null&&shEv>12&&ps<4.5){
    add('Evaporador subalimentado','Superheat alto junto con presión de succión baja: patrón compatible con evaporador recibiendo poco refrigerante.',[
      'Carga insuficiente','Restricción en filtro deshidratador/línea líquida','TXV/EEV restringida o con problema de control','Baja carga térmica/flujo de aire'
    ],['Inspeccionar flujo de aire.','Medir caída de temperatura en filtro deshidratador.','Revisar TXV/EEV y procedimiento de carga.'],'review');
  }

  // Carga insuficiente: requiere SC bajo
  if(shEv!==null&&shEv>12&&sc!==null&&sc<3){
    add('Patrón compatible con carga insuficiente','Superheat alto + subcooling bajo. La combinación aumenta la evidencia de carga insuficiente, pero no la confirma por sí sola.',[
      'Fuga de refrigerante','Carga insuficiente','Restricción o condición anormal del sistema'
    ],['Buscar fugas antes de agregar refrigerante.','Confirmar subcooling/superheat después de estabilizar el equipo.'],'review');
  }

  // Restricción
  if(shEv!==null&&shEv>12&&sc!==null&&sc>=5){
    add('Patrón compatible con restricción','Superheat alto + subcooling normal/alto puede ser compatible con restricción antes del evaporador.',[
      'Filtro deshidratador restringido','Solenoide/válvula parcialmente cerrada','TXV/EEV restringida','Línea líquida obstruida'
    ],['Medir temperatura antes y después del filtro deshidratador.','Inspeccionar válvulas y dispositivo de expansión.'],'review');
  }

  // Condensador
  if(tcond!==null&&tamb!==null&&dtCond>17&&pd>18){
    add('Condensación elevada','Presión y temperatura de condensación altas junto con ΔT condensación-ambiente elevado: patrón compatible con rechazo de calor deficiente.',[
      'Serpentín del condensador sucio','Flujo de aire insuficiente','Ventilador con problema','Recirculación de aire caliente','Ambiente muy elevado'
    ],['Inspeccionar serpentín y ventilador.','Verificar sentido y caudal de aire.','Buscar recirculación de aire caliente.'],'review');
  }

  // Sobre carga
  if(sc!==null&&sc>12&&pd>18){
    add('Subcooling alto + descarga elevada','Patrón compatible con exceso de carga, pero primero deben descartarse problemas de rechazo de calor.',[
      'Exceso de refrigerante','Condensador con rechazo de calor deficiente','Carga térmica/condiciones ambientales particulares'
    ],['Verificar limpieza y flujo de aire del condensador antes de retirar refrigerante.','Confirmar condición con procedimiento del fabricante.'],'attention');
  }

  // Airflow
  if(dtAir!==null&&dtAir<7&&shEv!==null&&shEv>10){
    add('Posible problema de flujo de aire / carga térmica','ΔT de aire bajo con superheat alto puede ser compatible con flujo de aire o carga térmica fuera de condición.',[
      'Filtro sucio','Evaporador sucio','Ventilador/caudal insuficiente','Carga térmica baja'
    ],['Revisar filtro, serpentín, ventilador y flujo de aire.'],'attention');
  }

  // Descarga
  if(tdis!==null&&tdis>110){
    add('Temperatura de descarga elevada','La descarga está elevada. La causa debe correlacionarse con superheat, presión de descarga y condiciones de condensación.',[
      'Superheat excesivo','Condensación elevada','Carga insuficiente','Restricción','Problema de enfriamiento del compresor'
    ],['Verificar superheat total.','Verificar presión/temperatura de condensación.','Revisar enfriamiento del compresor.'],'review');
  }

  // Eléctrico
  if(iPct!==null&&iPct>115){
    add('Corriente por encima de nominal','La corriente medida supera 115% de la nominal ingresada. No significa automáticamente compresor defectuoso.',[
      'Alta presión de condensación','Problema mecánico del compresor','Tensión de alimentación incorrecta','Problema eléctrico','Condición de carga elevada'
    ],['Verificar voltaje bajo carga.','Correlacionar corriente con presión de descarga.','Inspeccionar conexiones y condición mecánica.'],'review');
  } else if(iPct!==null&&iPct<70){
    add('Corriente significativamente baja','La corriente está muy por debajo de la nominal. Puede depender de carga, capacidad, condición del compresor o medición.',[
      'Baja carga térmica','Baja carga de refrigerante','Compresor descargado','Problema de medición'
    ],['Confirmar condición de operación y estabilidad.','Comparar con especificación del fabricante.'],'attention');
  }

  if(findings.length===0){
    add('Sin patrón de falla fuerte','Las mediciones no muestran uno de los patrones de alerta configurados. Esto no equivale a una certificación de funcionamiento perfecto.',[
      'Condición normal','Datos insuficientes para discriminar una falla'
    ],['Confirmar estabilidad de operación.','Comparar con datos del fabricante.'],'normal');
  }

  let worst='normal';
  const rank={normal:0,attention:1,review:2,critical:3};
  findings.forEach(f=>{if(rank[f.level]>rank[worst])worst=f.level});
  const labels={normal:'NORMAL',attention:'ATENCIÓN',review:'REVISAR',critical:'CRÍTICO'};
  const summaries={
    normal:'No se detectó un patrón fuerte de alerta con las mediciones ingresadas.',
    attention:'Existe una condición que merece revisión, pero la evidencia no es suficiente para afirmar una falla.',
    review:'Existe un patrón compatible con una anomalía. Realice la comprobación indicada antes de intervenir.',
    critical:'Existe una condición potencialmente riesgosa. Priorice la verificación antes de continuar operando.'
  };
  setStatus(worst,labels[worst],summaries[worst]);

  document.getElementById('findings').innerHTML=findings.map(f=>
    `<div class="alert ${f.level==='critical'?'danger':f.level==='normal'?'ok':''}"><b>${f.title}</b><br>${f.detail}</div>`).join('');
  document.getElementById('causes').innerHTML=[...causes].map(c=>`<li>${c}</li>`).join('')||'<li>No disponibles.</li>';
  document.getElementById('next').innerHTML=[...new Set(next)].map(n=>`<div class="alert">${n}</div>`).join('')||'<div class="alert">Compare con datos del fabricante.</div>';
}
function renderDefault(){
  document.getElementById('metrics').innerHTML=[
    'T° saturación evaporación','T° saturación condensación','Superheat evaporador','Superheat total','Subcooling','ΔT aire retorno-suministro','ΔT condensación-ambiente','Relación de presión','Desvío de voltaje','Corriente vs nominal'
  ].map(x=>metric(x,null)).join('');
  document.getElementById('findings').innerHTML='<div class="alert">Complete las mediciones disponibles y ejecute el diagnóstico.</div>';
  document.getElementById('causes').innerHTML='<li>Datos insuficientes.</li>';
  document.getElementById('next').innerHTML='<div class="alert">Ingrese presión de succión y descarga para comenzar.</div>';
}
function saveData(){
  const ids=['brand','model','type','ref','capacity','compressor','phases','freq','tamb','treturn','tsupply','ambientSource','psuc','punit','pdis','punit2','tevapout','tsuction','tliquid','tdischarge','vmeas','vnom','ameas','anom','notes'];
  const d={};ids.forEach(id=>d[id]=val(id));localStorage.setItem('hvacrV2',JSON.stringify(d));alert('Datos guardados en este navegador.');
}
function loadData(){
  const d=JSON.parse(localStorage.getItem('hvacrV2')||'null');if(!d){alert('No hay datos guardados.');return}
  Object.entries(d).forEach(([id,v])=>{if(document.getElementById(id))document.getElementById(id).value=v});
  diagnose();
}
function clearData(){
  if(!confirm('¿Limpiar las mediciones y datos del formulario?'))return;
  document.querySelectorAll('input,textarea').forEach(x=>x.value='');
  document.getElementById('type').value='Split';document.getElementById('ref').value='R410A';document.getElementById('compressor').value='No identificado';document.getElementById('phases').value='1';document.getElementById('ambientSource').value='Medición de campo';
  renderDefault();setStatus('error','DATOS INSUFICIENTES','Ingrese las mediciones disponibles.');
}
document.querySelectorAll('input,select').forEach(el=>el.addEventListener('change',()=>{if(el.closest('.card')) diagnose()}));
renderDefault();
</script>
</body>
</html>
