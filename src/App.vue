<script setup>
import { ref } from "vue";

// adding a state to the modal
const showModal = ref(false);

// adding a state to the textarea
const newNote = ref("");

// a state array to store notes
const notes = ref([]);

// function to generate random color
function getRandomColor() {
  return "hsl(" + Math.random() * 360 + ", 100%, 75%)";
}

// handler for add note click event
const addNote = () => {
  notes.value.push({
    id: Math.floor(Math.random() * 1000000),
    text: newNote.value,
    date: new Date(),
    backgroundColor: getRandomColor()
  })

  // update show modal to close modal window
  showModal.value = false;

  // clear textarea after adding a new note
  newNote.value = "";
}

</script>

<template>
  <main>
    <!-- render page if showModal is true -->
    <div v-if="showModal" class="overlay">
      <div class="modal">
        <!-- add two way binding using model directive -->
        <textarea v-model="newNote" name="note" id="note" cols="30" rows="10"></textarea>

        <button @click="addNote">Add Note</button>

        <button @click="showModal = false" class="close">Close</button>

      </div>
    </div>

    <div class="container">
      <header>
        <h1>Notes</h1>
        <button @click="showModal = true">+</button>
      </header>

      <div class="cards-container">
        <div class="card">
          <p class="main-text">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Corrupti iusto ipsum dolor quia harum veniam neque!
            Ex nobis, omnis consequuntur doloremque quis quibusdam debitis, error blanditiis
          </p>
          <p class="date">
            31/03/2023
          </p>
        </div>

        <div class="card">
          <p class="main-text">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Corrupti iusto ipsum dolor quia harum veniam neque!
            Ex nobis, omnis consequuntur doloremque quis quibusdam debitis, error blanditiis
          </p>
          <p class="date">
            31/03/2023
          </p>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  width: 100vw;
  background-color: white;
  color: black;
}

.container {
  max-width: 1000px;
  padding: 10px;
  margin: 0 auto;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  font-weight: bold;
  margin-bottom: 25px;
  font-size: 70px;

}

header button {
  border: none;
  padding: 10px;
  width: 50px;
  height: 50px;
  cursor: pointer;
  background-color: rgb(21, 20, 20);
  border-radius: 100%;
  color: white;
  font-size: 20px;
}

.card {
  width: 225px;
  height: 225px;
  background-color: rgb(237, 182, 44);
  padding: 10px;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-bottom: 20px;
  margin-right: 10px;
}

.date {
  font-size: 12.5px;
  font-weight: bold;
}

.cards-container {
  display: flex;
  flex-wrap: wrap;
}

.main-text {
  font-size: 14px;
}

.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.77);
  z-index: 10;
  display: flex;
  align-items: center;
  justify-content: center;
}

.modal {
  width: 750px;
  border-radius: 10px;
  background-color: white;
  padding: 30px;
  position: relative;
  display: flex;
  flex-direction: column;
}

.modal button {
  padding: 10px 20px;
  font-size: 20px;
  width: 100%;
  background-color: blueviolet;
  color: white;
  border: none;
  cursor: pointer;
  margin-top: 15px;
  border-radius: 30px;
}

.modal .close {
  background-color: rgb(193, 15, 15);
  margin-top: 7px;
}
</style>