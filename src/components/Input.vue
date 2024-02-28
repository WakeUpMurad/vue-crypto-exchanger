<template>
  <input min="0" type="number" @input="changeAmound($event.target.value)"><br>
  <button @click="convert()">Конвертировать</button>
  <button @click="favourite()" className="fuv-button">В избранное</button>
</template>

<script>
export default {
  props: {
    changeAmound: {
      type: Function,
      required: true
    },
    convert: {
      type: Function,
      required: true
    },
    favourite: {
      type: Function,
      required: true
    }
  }
}
</script>

<style scoped>
input {
  width: 500px;
  position: relative;
  top: -50px;
  font-size: 1.25rem;
  border-radius: 3px;
  border: 4px solid #1a032d;
  padding: 10px 15px;
  background: #fafafa;
}

button {
  position: relative;
  top: -20px;
  padding: 10px 15px;
  color: #fff;
  text-transform: uppercase;
  cursor: pointer;
  background: #1a032d;
}

button.fuv-button {
  margin-left: 20px;
}
</style>