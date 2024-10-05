<script>
export default {
  name: "App",
  data() {
    return {
      usuario: {
        titulo: "",
        emoji: "",
        apreciacion: "",
        competencias: [],
        opinion: "",
      },
    };
  },
};
</script>
<template>
  <div class="container">
    <div class="contenido">
      <div class="formulario border p-4 rounded shadow bg-dark">
        <form class="text-light">
          <div class="mb-3">
            <label class="form-label">Título :</label>
            <input class="text" type="text" v-model="usuario.titulo" />
          </div>
          <hr>
          <div class="mb-3">
            <label class="text">Emoji</label>
            <select class="form-select" v-model="usuario.emoji">
              <option value="🦹">🦹</option>
              <option value="👩‍💻">👩‍💻</option>
              <option value="🥷">🥷</option>
              <option value="🧑‍🏫">🧑‍🏫</option>
            </select>
          </div>
          <hr>
          <div class="mb-3">
            <label class="form-label">Apreciación</label>
            <div class="d-flex gap-3">
              <div class="form-check">
                <input class="form-check-input" type="radio" name="flexRadioDefault" id="r" value="Regular" v-model="usuario.apreciacion" />
                <label class="form-check-label fw-normal" for="r">
                  Regular
                </label>
              </div>
              <div class="form-check">
                <input class="form-check-input" type="radio" name="flexRadioDefault" id="b" value="Bien" v-model="usuario.apreciacion" />
                <label class="form-check-label fw-normal" for="b">
                  Bien
                </label>
              </div>
              <div class="form-check">
                <input class="form-check-input" type="radio" name="flexRadioDefault" id="mb" value="Muy bien !" v-model="usuario.apreciacion" />
                <label class="form-check-label fw-normal" for="mb">
                  Muy Bien
                </label>
              </div>
              <div class="form-check">
                <input class="form-check-input" type="radio" name="flexRadioDefault" id="n" value="Normal " v-model="usuario.apreciacion" />
                <label class="form-check-label fw-normal" for="n">
                  Normal
                </label>
              </div>
            </div>
          </div>
          <hr>
          <div class="mb-3">

<label class="form-label">Competencias aprendidas </label>
<br>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="componente" value="Morfologia de un componente"
    v-model="usuario.competencias" />
  <label class="form-check-label" for="componente"> Morfologia de un componente </label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="directivas" value="Directivas" v-model="usuario.competencias" />
  <label class="form-check-label" for="directivas"> Directivas </label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="databinding" value="One-Way y TwO-Way data binding" v-model="usuario.competencias" />
  <label class="form-check-label" for="databinding"> One-Way y TwO-Way data binding</label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="estado" value="Estado" v-model="usuario.competencias" />
  <label class="form-check-label" for="estado"> Estado </label>
</div>
<div class="form-check form-check-inline">
  <input class="form-check-input" type="checkbox" id="patrondiseño" value="El patrón de diseño MVVM"
    v-model="usuario.competencias" />
  <label class="form-check-label" for="patrondiseño"> El patrón de diseño MVVM </label>
</div>
</div>
<hr>
<div class="mb-3">
<label class="form-label">Opinion</label>
<textarea class="form-control" v-model="usuario.opinion"></textarea>
</div>

        </form>
      </div>

      <div class="respuestas">
        <div class="border p-4 rounded shadow bg-light">
          <h1 class="text">{{ usuario.emoji }}</h1>
          <h2 class="bg-light text-dark"> {{ usuario.titulo }}</h2>
          <h3>Y me parece  {{ usuario.apreciacion }}</h3>
          <h4>{{ usuario.competencias.join(' -- ') }}</h4>
          <h5>Mi opinión del framwork hasta ahora es :</h5>
          <h6>{{ usuario.opinion }}</h6>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.container {
  width: 100%;
  display: flex;
  justify-content: center;
}

.contenido {
  display: flex;
  justify-content: space-between;
  gap: 20px;
  width: 100%;
  max-width: 1200px; /* Máximo ancho del contenedor */
}

.formulario {
  flex: 1;
  max-width: 500px; /* Limita el tamaño del formulario */
}

.respuestas {
  flex: 1;
  max-width: 500px; /* Limita el tamaño del área de respuestas */
}

</style>
