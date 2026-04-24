<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lista de Espera — Neuromodulación NESA | Clínica Dra. Diana Isis Becerril</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #F7F3EE;
    --warm-white: #FDFBF8;
    --sage: #7A8C78;
    --sage-light: #B5C4B2;
    --sage-dark: #4A5F48;
    --terracotta: #C4896A;
    --charcoal: #2C2C2A;
    --charcoal-light: #5A5A57;
    --gold: #B8965A;
    --border: rgba(44,44,42,0.1);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--charcoal);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Background pattern */
  body::before {
    content: '';
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    background-image: 
      radial-gradient(circle at 20% 20%, rgba(122,140,120,0.06) 0%, transparent 50%),
      radial-gradient(circle at 80% 80%, rgba(196,137,106,0.05) 0%, transparent 50%),
      url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%237A8C78' fill-opacity='0.03'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 0;
  }

  .container {
    position: relative;
    z-index: 1;
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  /* LEFT PANEL */
  .left-panel {
    background: var(--sage-dark);
    padding: 60px 56px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    position: relative;
    overflow: hidden;
  }

  .left-panel::before {
    content: '';
    position: absolute;
    top: -100px; right: -100px;
    width: 400px; height: 400px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(184,150,90,0.15) 0%, transparent 70%);
  }

  .left-panel::after {
    content: '';
    position: absolute;
    bottom: -60px; left: -60px;
    width: 300px; height: 300px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(122,140,120,0.3) 0%, transparent 70%);
  }

  .logo-area {
    position: relative;
    z-index: 2;
  }

  .logo-mark {
    width: 44px; height: 44px;
    border: 1.5px solid rgba(255,255,255,0.4);
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 20px;
  }

  .logo-mark svg {
    width: 20px; height: 20px;
    fill: none;
    stroke: rgba(255,255,255,0.8);
    stroke-width: 1.5;
  }

  .doctor-name {
    font-family: 'DM Sans', sans-serif;
    font-weight: 300;
    font-size: 13px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.5);
    margin-bottom: 6px;
  }

  .clinic-name {
    font-family: 'DM Sans', sans-serif;
    font-weight: 400;
    font-size: 13px;
    color: rgba(255,255,255,0.7);
  }

  .main-content {
    position: relative;
    z-index: 2;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: rgba(184,150,90,0.2);
    border: 1px solid rgba(184,150,90,0.4);
    border-radius: 100px;
    padding: 6px 14px;
    margin-bottom: 32px;
  }

  .badge-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--gold);
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.8); }
  }

  .badge-text {
    font-size: 11px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--gold);
    font-weight: 500;
  }

  .headline {
    font-family: 'Cormorant Garamond', serif;
    font-weight: 300;
    font-size: 52px;
    line-height: 1.1;
    color: #fff;
    margin-bottom: 24px;
  }

  .headline em {
    font-style: italic;
    color: var(--sage-light);
  }

  .description {
    font-size: 15px;
    font-weight: 300;
    color: rgba(255,255,255,0.65);
    line-height: 1.7;
    margin-bottom: 40px;
    max-width: 380px;
  }

  .features {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .feature {
    display: flex;
    align-items: flex-start;
    gap: 14px;
  }

  .feature-icon {
    width: 32px; height: 32px;
    border-radius: 8px;
    background: rgba(255,255,255,0.08);
    border: 1px solid rgba(255,255,255,0.12);
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
    font-size: 14px;
  }

  .feature-text {
    font-size: 13px;
    color: rgba(255,255,255,0.65);
    line-height: 1.5;
    padding-top: 6px;
  }

  .feature-text strong {
    color: rgba(255,255,255,0.9);
    font-weight: 500;
    display: block;
    margin-bottom: 2px;
  }

  .opening-info {
    position: relative;
    z-index: 2;
    display: flex;
    align-items: center;
    gap: 16px;
    padding: 20px 0;
    border-top: 1px solid rgba(255,255,255,0.1);
  }

  .countdown-label {
    font-size: 11px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: rgba(255,255,255,0.4);
    margin-bottom: 4px;
  }

  .countdown-value {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px;
    color: rgba(255,255,255,0.9);
    font-weight: 300;
  }

  .divider-vert {
    width: 1px;
    height: 36px;
    background: rgba(255,255,255,0.15);
  }

  /* RIGHT PANEL */
  .right-panel {
    background: var(--warm-white);
    padding: 60px 56px;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .form-header {
    margin-bottom: 40px;
  }

  .form-eyebrow {
    font-size: 11px;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--sage);
    margin-bottom: 10px;
  }

  .form-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 36px;
    font-weight: 400;
    color: var(--charcoal);
    line-height: 1.2;
    margin-bottom: 12px;
  }

  .form-subtitle {
    font-size: 14px;
    color: var(--charcoal-light);
    line-height: 1.6;
  }

  .form-group {
    margin-bottom: 20px;
  }

  label {
    display: block;
    font-size: 12px;
    font-weight: 500;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    color: var(--charcoal-light);
    margin-bottom: 8px;
  }

  input {
    width: 100%;
    padding: 14px 18px;
    border: 1.5px solid var(--border);
    border-radius: 10px;
    background: var(--cream);
    font-family: 'DM Sans', sans-serif;
    font-size: 15px;
    font-weight: 300;
    color: var(--charcoal);
    transition: all 0.2s ease;
    outline: none;
    -webkit-appearance: none;
  }

  input::placeholder {
    color: rgba(44,44,42,0.3);
  }

  input:focus {
    border-color: var(--sage);
    background: #fff;
    box-shadow: 0 0 0 4px rgba(122,140,120,0.1);
  }

  input.error {
    border-color: var(--terracotta);
  }

  .error-msg {
    font-size: 12px;
    color: var(--terracotta);
    margin-top: 6px;
    display: none;
  }

  .error-msg.visible {
    display: block;
  }

  .submit-btn {
    width: 100%;
    padding: 16px 24px;
    background: var(--sage-dark);
    color: #fff;
    border: none;
    border-radius: 10px;
    font-family: 'DM Sans', sans-serif;
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.04em;
    cursor: pointer;
    transition: all 0.25s ease;
    margin-top: 8px;
    position: relative;
    overflow: hidden;
  }

  .submit-btn:hover {
    background: var(--charcoal);
    transform: translateY(-1px);
    box-shadow: 0 8px 24px rgba(44,44,42,0.2);
  }

  .submit-btn:active {
    transform: translateY(0);
  }

  .submit-btn:disabled {
    opacity: 0.6;
    cursor: not-allowed;
    transform: none;
  }

  .btn-content {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
  }

  .btn-spinner {
    display: none;
    width: 16px; height: 16px;
    border: 2px solid rgba(255,255,255,0.3);
    border-top-color: #fff;
    border-radius: 50%;
    animation: spin 0.7s linear infinite;
  }

  @keyframes spin { to { transform: rotate(360deg); } }

  .btn-arrow {
    transition: transform 0.2s ease;
  }

  .submit-btn:hover .btn-arrow {
    transform: translateX(3px);
  }

  .privacy-note {
    font-size: 12px;
    color: var(--charcoal-light);
    text-align: center;
    margin-top: 16px;
    opacity: 0.7;
    line-height: 1.5;
  }

  .privacy-note a {
    color: var(--sage-dark);
    text-decoration: none;
  }

  /* SUCCESS STATE */
  .success-state {
    display: none;
    text-align: center;
    padding: 20px 0;
    animation: fadeInUp 0.5s ease;
  }

  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  .success-icon {
    width: 64px; height: 64px;
    background: linear-gradient(135deg, var(--sage), var(--sage-dark));
    border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 24px;
    font-size: 28px;
  }

  .success-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 32px;
    font-weight: 400;
    color: var(--charcoal);
    margin-bottom: 12px;
  }

  .success-text {
    font-size: 15px;
    color: var(--charcoal-light);
    line-height: 1.6;
    margin-bottom: 24px;
  }

  .success-number {
    display: inline-block;
    background: var(--cream);
    border: 1.5px solid var(--border);
    border-radius: 10px;
    padding: 14px 28px;
  }

  .success-number-label {
    font-size: 11px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--sage);
    margin-bottom: 4px;
  }

  .success-number-value {
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px;
    font-weight: 400;
    color: var(--charcoal);
  }

  .spots-counter {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-top: 28px;
    padding: 12px 16px;
    background: rgba(122,140,120,0.08);
    border-radius: 8px;
    border: 1px solid rgba(122,140,120,0.2);
  }

  .spots-text {
    font-size: 13px;
    color: var(--sage-dark);
    font-weight: 400;
  }

  .spots-count {
    font-weight: 500;
    color: var(--terracotta);
  }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    .container {
      grid-template-columns: 1fr;
    }

    .left-panel {
      padding: 48px 32px;
      min-height: auto;
    }

    .headline {
      font-size: 40px;
    }

    .right-panel {
      padding: 48px 32px;
    }

    .features {
      display: none;
    }
  }

  @media (max-width: 480px) {
    .left-panel, .right-panel {
      padding: 36px 24px;
    }

    .headline {
      font-size: 34px;
    }

    .form-title {
      font-size: 28px;
    }
  }

  /* Stagger animation on load */
  .form-group { animation: fadeInUp 0.4s ease both; }
  .form-group:nth-child(1) { animation-delay: 0.1s; }
  .form-group:nth-child(2) { animation-delay: 0.2s; }
  .form-group:nth-child(3) { animation-delay: 0.3s; }
  .submit-btn { animation: fadeInUp 0.4s ease 0.4s both; }
</style>
</head>
<body>

<div class="container">

  <!-- LEFT PANEL -->
  <div class="left-panel">
    <div class="logo-area">
      <div class="logo-mark">
        <svg viewBox="0 0 24 24">
          <circle cx="12" cy="12" r="9"/>
          <path d="M12 7v5l3 3" stroke-linecap="round"/>
        </svg>
      </div>
      <div class="doctor-name">Dra. Diana Isis Becerril</div>
      <div class="clinic-name">Psiconeuroinmunóloga · Medicina de Precisión</div>
    </div>

    <div class="main-content">
      <div class="badge">
        <div class="badge-dot"></div>
        <span class="badge-text">Apertura en 2 meses</span>
      </div>

      <h1 class="headline">
        La terapia que<br>
        <em>recalibra</em> tu<br>
        sistema nervioso
      </h1>

      <p class="description">
        Neuromodulación no invasiva NESA® — la primera clínica en México con esta tecnología dentro de un modelo de medicina integrativa y PNEI.
      </p>

      <div class="features">
        <div class="feature">
          <div class="feature-icon">⚡</div>
          <div class="feature-text">
            <strong>Sin agujas. Sin medicamentos.</strong>
            Microcorrientes que hablan el idioma de tu sistema nervioso.
          </div>
        </div>
        <div class="feature">
          <div class="feature-icon">🧠</div>
          <div class="feature-text">
            <strong>Eje intestino-mente-cuerpo</strong>
            Tratamiento que actúa en la raíz, no en el síntoma.
          </div>
        </div>
        <div class="feature">
          <div class="feature-icon">📊</div>
          <div class="feature-text">
            <strong>Evidencia científica</strong>
            +20 estudios publicados en revistas indexadas internacionales.
          </div>
        </div>
      </div>
    </div>

    <div class="opening-info">
      <div>
        <div class="countdown-label">Apertura</div>
        <div class="countdown-value">Junio 2026</div>
      </div>
      <div class="divider-vert"></div>
      <div>
        <div class="countdown-label">Ubicación</div>
        <div class="countdown-value">Polanco · CDMX</div>
      </div>
    </div>
  </div>

  <!-- RIGHT PANEL -->
  <div class="right-panel">

    <div id="form-container">
      <div class="form-header">
        <div class="form-eyebrow">Lista de espera</div>
        <h2 class="form-title">Reserva tu lugar</h2>
        <p class="form-subtitle">
          Sé de las primeras personas en acceder a la terapia NESA en México. Los lugares de la lista son limitados.
        </p>
      </div>

      <form id="waitlist-form" novalidate>
        <div class="form-group">
          <label for="nombre">Nombre completo</label>
          <input 
            type="text" 
            id="nombre" 
            name="nombre"
            placeholder="Tu nombre completo"
            autocomplete="name"
          >
          <div class="error-msg" id="error-nombre">Por favor ingresa tu nombre completo.</div>
        </div>

        <div class="form-group">
          <label for="celular">Número de celular</label>
          <input 
            type="tel" 
            id="celular" 
            name="celular"
            placeholder="+52 55 0000 0000"
            autocomplete="tel"
          >
          <div class="error-msg" id="error-celular">Por favor ingresa un número de celular válido.</div>
        </div>

        <div class="form-group">
          <label for="email">Correo electrónico</label>
          <input 
            type="email" 
            id="email" 
            name="email"
            placeholder="tu@correo.com"
            autocomplete="email"
          >
          <div class="error-msg" id="error-email">Por favor ingresa un correo electrónico válido.</div>
        </div>

        <button type="submit" class="submit-btn" id="submit-btn">
          <div class="btn-content">
            <div class="btn-spinner" id="btn-spinner"></div>
            <span id="btn-text">Quiero mi lugar en la lista</span>
            <span class="btn-arrow" id="btn-arrow">→</span>
          </div>
        </button>

        <p class="privacy-note">
          Tu información es confidencial y solo se usará para contactarte sobre la apertura de la clínica.
        </p>
      </form>

      <div class="spots-counter">
        <span>🩺</span>
        <span class="spots-text">
          Lugares disponibles en lista: <span class="spots-count" id="spots-count">—</span>
        </span>
      </div>
    </div>

    <!-- SUCCESS STATE -->
    <div class="success-state" id="success-state">
      <div class="success-icon">✓</div>
      <h3 class="success-title">¡Estás en la lista!</h3>
      <p class="success-text">
        Pronto te contactaremos con todos los detalles sobre la apertura y cómo agendar tu primera sesión de NESA.
      </p>
      <div class="success-number">
        <div class="success-number-label">Tu número de registro</div>
        <div class="success-number-value" id="registro-numero">#—</div>
      </div>
    </div>

  </div>
</div>

<script>
// ─── CONFIG ───────────────────────────────────────────────
// Para conectar con Notion, reemplaza estos valores:
const NOTION_TOKEN = 'TU_INTEGRATION_TOKEN'; // Token de integración de Notion
const DATABASE_ID  = 'dc053f0da2bc4522b07ff8a6bbfa20e0'; // ID de la base de datos creada
// ──────────────────────────────────────────────────────────

let registroActual = 0;

// Simulate spots (reemplazar con query real si se conecta a Notion)
async function cargarContadorLugares() {
  try {
    document.getElementById('spots-count').textContent = '30 disponibles';
  } catch(e) {
    document.getElementById('spots-count').textContent = 'Limitados';
  }
}

cargarContadorLugares();

// ─── VALIDACIÓN ───────────────────────────────────────────
function validarCampo(id, errorId, validador) {
  const input = document.getElementById(id);
  const error = document.getElementById(errorId);
  const valido = validador(input.value.trim());
  
  if (!valido) {
    input.classList.add('error');
    error.classList.add('visible');
  } else {
    input.classList.remove('error');
    error.classList.remove('visible');
  }
  return valido;
}

function esEmailValido(email) {
  return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
}

function esTelefonoValido(tel) {
  return tel.replace(/[\s\-\+\(\)]/g, '').length >= 8;
}

// ─── SUBMIT ───────────────────────────────────────────────
document.getElementById('waitlist-form').addEventListener('submit', async function(e) {
  e.preventDefault();

  const nombreOk  = validarCampo('nombre',  'error-nombre',  v => v.length >= 2);
  const celularOk = validarCampo('celular', 'error-celular', esTelefonoValido);
  const emailOk   = validarCampo('email',   'error-email',   esEmailValido);

  if (!nombreOk || !celularOk || !emailOk) return;

  const nombre  = document.getElementById('nombre').value.trim();
  const celular = document.getElementById('celular').value.trim();
  const email   = document.getElementById('email').value.trim();

  // UI: loading state
  const btn = document.getElementById('submit-btn');
  const spinner = document.getElementById('btn-spinner');
  const btnText = document.getElementById('btn-text');
  const btnArrow = document.getElementById('btn-arrow');

  btn.disabled = true;
  spinner.style.display = 'block';
  btnText.textContent = 'Registrando...';
  btnArrow.style.display = 'none';

  try {
    // Calcular número de registro
    const ahora = new Date();
    registroActual++;
    const numRegistro = registroActual;

    // ── OPCIÓN A: Envío directo a Notion API ──────────────────
    // Solo funciona si tu token tiene acceso público (raro en producción).
    // Para producción, usar un backend/serverless function.
    
    const payload = {
      parent: { database_id: DATABASE_ID },
      properties: {
        "Nombre Completo": {
          title: [{ text: { content: nombre } }]
        },
        "Email": { email: email },
        "Número de Celular": { phone_number: celular },
        "N° Registro": { number: numRegistro },
        "Fecha de Registro": {
          date: { start: ahora.toISOString().split('T')[0] }
        },
        "Estado": {
          select: { name: "En lista" }
        }
      }
    };

    // DESCOMENTA para conectar con Notion (requiere proxy o backend):
    /*
    const res = await fetch('https://api.notion.com/v1/pages', {
      method: 'POST',
      headers: {
        'Authorization': `Bearer ${NOTION_TOKEN}`,
        'Content-Type': 'application/json',
        'Notion-Version': '2022-06-28'
      },
      body: JSON.stringify(payload)
    });

    if (!res.ok) throw new Error('Error en Notion API');
    */

    // ── OPCIÓN B (ACTUAL): Guardar localmente + CSV download ──
    // Mientras no hay backend, guardamos en localStorage y ofrecemos CSV
    const registros = JSON.parse(localStorage.getItem('nesa_waitlist') || '[]');
    const nuevoRegistro = {
      numero: registros.length + 1,
      nombre,
      celular,
      email,
      fecha: ahora.toLocaleString('es-MX'),
      timestamp: ahora.toISOString()
    };
    registros.push(nuevoRegistro);
    localStorage.setItem('nesa_waitlist', JSON.stringify(registros));
    
    const numeroFinal = nuevoRegistro.numero;

    // Mostrar éxito
    document.getElementById('form-container').style.display = 'none';
    const successState = document.getElementById('success-state');
    successState.style.display = 'block';
    document.getElementById('registro-numero').textContent = `#${String(numeroFinal).padStart(3, '0')}`;

  } catch (err) {
    btn.disabled = false;
    spinner.style.display = 'none';
    btnText.textContent = 'Quiero mi lugar en la lista';
    btnArrow.style.display = 'inline';
    alert('Hubo un error al procesar tu solicitud. Por favor intenta de nuevo.');
    console.error(err);
  }
});

// ─── INPUT LIVE VALIDATION ────────────────────────────────
['nombre', 'celular', 'email'].forEach(id => {
  document.getElementById(id).addEventListener('blur', function() {
    this.classList.remove('error');
    document.getElementById(`error-${id}`).classList.remove('visible');
  });
});

// ─── ADMIN: Descargar CSV (abrir consola y ejecutar: descargarCSV()) ──
window.descargarCSV = function() {
  const registros = JSON.parse(localStorage.getItem('nesa_waitlist') || '[]');
  if (!registros.length) { alert('No hay registros aún.'); return; }
  
  const headers = ['N° Registro', 'Nombre Completo', 'Número de Celular', 'Email', 'Fecha de Registro'];
  const rows = registros.map(r => [
    r.numero, 
    `"${r.nombre}"`, 
    r.celular, 
    r.email, 
    r.fecha
  ]);
  
  const csv = [headers.join(','), ...rows.map(r => r.join(','))].join('\n');
  const blob = new Blob(['\uFEFF' + csv], { type: 'text/csv;charset=utf-8;' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = `lista_espera_nesa_${new Date().toISOString().split('T')[0]}.csv`;
  a.click();
  URL.revokeObjectURL(url);
};

// ─── ADMIN: Ver registros en consola ──────────────────────
window.verRegistros = function() {
  const r = JSON.parse(localStorage.getItem('nesa_waitlist') || '[]');
  console.table(r);
  return r;
};
</script>

</body>
</html>
