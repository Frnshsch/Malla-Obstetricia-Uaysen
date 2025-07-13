<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Malla Interactiva Obstetricia</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Malla Interactiva - Obstetricia</h1>
  <div class="grid">
    <div class="ramo" data-id="fundamentos_profesion" data-depends="salud1">
      <input type="checkbox" id="fundamentos_profesion" />
      <label for="fundamentos_profesion">Fundamentos disciplinarios de la profesión</label>
    </div>
    <div class="ramo" data-id="quimica_bioquimica" data-depends="biologia,fisiologia">
      <input type="checkbox" id="quimica_bioquimica" />
      <label for="quimica_bioquimica">Química y bioquímica</label>
    </div>
    <div class="ramo" data-id="anatomia" data-depends="salud1,fisiologia">
      <input type="checkbox" id="anatomia" />
      <label for="anatomia">Anatomía</label>
    </div>
    <div class="ramo" data-id="sociocultural" data-depends="educacion">
      <input type="checkbox" id="sociocultural" />
      <label for="sociocultural">Fund. socioculturales de la salud</label>
    </div>
    <div class="ramo" data-id="formacion1" data-depends="formacion2">
      <input type="checkbox" id="formacion1" />
      <label for="formacion1">Formación fundamental I</label>
    </div>
    <div class="ramo" data-id="informatica" data-depends="">
      <input type="checkbox" id="informatica" />
      <label for="informatica">Herramientas informáticas</label>
    </div>
    <div class="ramo" data-id="salud1" data-depends="salud2">
      <input type="checkbox" id="salud1" />
      <label for="salud1">Salud de la mujer y RN I</label>
    </div>
    <div class="ramo" data-id="biologia" data-depends="fisiopato,inmunologia">
      <input type="checkbox" id="biologia" />
      <label for="biologia">Biología celular y genética</label>
    </div>
    <div class="ramo" data-id="fisiologia" data-depends="salud2,fisiopato,inmunologia">
      <input type="checkbox" id="fisiologia" />
      <label for="fisiologia">Fisiología general y de sistemas</label>
    </div>
    <div class="ramo" data-id="histologia" data-depends="salud2">
      <input type="checkbox" id="histologia" />
      <label for="histologia">Histología</label>
    </div>
    <div class="ramo" data-id="formacion2" data-depends="formacion3">
      <input type="checkbox" id="formacion2" />
      <label for="formacion2">Formación fundamental II</label>
    </div>
    <!-- ... (Sigue agregando los demás ramos siguiendo este formato; si lo deseas, puedo incluir los más de 50 restantes en otro bloque) -->
  </div>
  <script src="script.js"></script>
</body>
</html>
body {
  font-family: sans-serif;
  padding: 20px;
  background: #fff0f0;
  color: #333;
}

h1 {
  text-align: center;
  color: #a00;
}

.grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
}

.ramo {
  background: white;
  border: 2px solid #a00;
  padding: 10px 15px;
  border-radius: 8px;
  width: 240px;
  text-align: center;
  box-shadow: 1px 1px 5px rgba(0,0,0,0.1);
}

.ramo input[type="checkbox"] {
  margin-right: 10px;
  accent-color: red;
}

.ramo input:checked + label {
  text-decoration: line-through;
  color: #999;
}document.querySelectorAll('.ramo input').forEach(input => {
  input.addEventListener('change', updateDependencies);
});

function updateDependencies() {
  const checked = Array.from(document.querySelectorAll('.ramo input:checked')).map(el => el.id);

  document.querySelectorAll('.ramo').forEach(ramo => {
    const input = ramo.querySelector('input');
    const depends = ramo.dataset.depends?.split(',').filter(Boolean) || [];

    if (depends.length === 0) return;

    const allMet = depends.every(id => checked.includes(id));
    input.disabled = !allMet && !input.checked;
  });
}

// Inicializar estado al cargar
updateDependencies();
