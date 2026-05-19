<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Acceso GuestGCC Wi-Fi</title>

  <style>
    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      font-family:Arial, Helvetica, sans-serif;
    }

    body{
      background: linear-gradient(135deg,#0f172a,#1e293b);
      min-height:100vh;
      display:flex;
      justify-content:center;
      align-items:center;
      padding:20px;
      color:white;
    }

    .card{
      width:100%;
      max-width:420px;
      background:rgba(255,255,255,0.08);
      backdrop-filter: blur(12px);
      border:1px solid rgba(255,255,255,0.15);
      border-radius:24px;
      padding:32px;
      box-shadow:0 10px 35px rgba(0,0,0,0.35);
    }

   <!-- .logo{
      width:80px;
      height:80px;
      margin:0 auto 20px;
      border-radius:20px;
      background:white;
      display:flex;
      justify-content:center;
      align-items:center;
      font-size:38px;
    }
-->
    .logo img{
  width:100%;
  height:100%;
  object-fit:contain;
  padding:10px;
}
    
    h1{
      text-align:center;
      margin-bottom:10px;
      font-size:30px;
      font-weight:bold;
    }

    .subtitle{
      text-align:center;
      color:#cbd5e1;
      margin-bottom:28px;
      line-height:1.5;
      font-size:15px;
    }

    .info-box{
      background:rgba(255,255,255,0.08);
      border-radius:18px;
      padding:18px;
      margin-bottom:16px;
    }

    .label{
      color:#94a3b8;
      font-size:13px;
      margin-bottom:6px;
    }

    .value{
      font-size:20px;
      font-weight:bold;
      word-break:break-word;
    }

    .copy-btn{
      margin-top:12px;
      width:100%;
      border:none;
      background:#38bdf8;
      color:#0f172a;
      padding:12px;
      border-radius:12px;
      font-size:15px;
      font-weight:bold;
      cursor:pointer;
      transition:0.2s;
    }

    .copy-btn:hover{
      background:#7dd3fc;
    }

    .steps{
      margin-top:24px;
    }

    .steps h2{
      font-size:18px;
      margin-bottom:12px;
    }

    .steps ol{
      padding-left:20px;
      color:#e2e8f0;
      line-height:1.8;
    }

    .footer{
      text-align:center;
      margin-top:28px;
      font-size:12px;
      color:#94a3b8;
    }

    @media(max-width:480px){
      .card{
        padding:24px;
      }

      h1{
        font-size:26px;
      }

      .value{
        font-size:18px;
      }
    }
  </style>
</head>
<body>

  <div class="card">

    <div class="logo">
  <img src="GCC LOGO.png" alt="Logo Empresa">
</div>

    <h1>GUESTGCC WI-FI</h1>

    <p class="subtitle">
      Utiliza las siguientes credenciales para acceder a la red.
    </p>

    <div class="info-box">
      <div class="label">Usuario</div>
      <div class="value" id="usuario">prueba123</div>

      <button class="copy-btn" onclick="copiar('usuario')">
        Copiar usuario
      </button>
    </div>

    <div class="info-box">
      <div class="label">Contraseña</div>
      <div class="value" id="password">abc123456</div>

      <button class="copy-btn" onclick="copiar('password')">
        Copiar contraseña
      </button>
    </div>

    <div class="steps">
      <h2>Instrucciones</h2>

      <ol>
        <li>Conéctate a la red Wi-Fi.</li>
        <li>Espera a ser redirigido al portal web</li>
        <li>Ingresa las credenciales en el portal cautivo.</li>
        <li>Disfruta tu conexión.</li>
      </ol>
    </div>

    <div class="footer">
      Acceso exclusivo para invitados
    </div>

  </div>

  <script>
    function copiar(id){
      const texto = document.getElementById(id).innerText;

      navigator.clipboard.writeText(texto).then(() => {
        alert("Copiado: " + texto);
      });
    }
  </script>

</body>
</html>
