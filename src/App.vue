<template>
  <main>
    <!-- <div class="overlay">
      <div class="modal">
        <textarea name="note" id="note" cols="30" rows="10"></textarea>
        <button>Add Note</button>
        <button class="close">Close</button>
      </div>
    </div> -->
    <div class="container">
      <header>
        <h1>Notes</h1>
        <button>+</button>
      </header>
      <div class="cards-container">
        <div class="card">
          <p class="main-text">
             Lorem ipsum, dolor sit amet consectetur adipisicing elit. Corrupti iusto ipsum dolor quia harum veniam neque! Ex nobis, omnis consequuntur doloremque quis quibusdam debitis, error blanditiis 
          </p>
          <p class="date">
            31/03/2023
          </p>
        </div>
        <div class="card">
          <p class="main-text">
             Lorem ipsum, dolor sit amet consectetur adipisicing elit. Corrupti iusto ipsum dolor quia harum veniam neque! Ex nobis, omnis consequuntur doloremque quis quibusdam debitis, error blanditiis 
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
  main{
    height: 100vh;
    width: 100vw;
    background-color: white;
    color: black;
  }

  .container{
    max-width: 1000px;
    padding: 10px;
    margin: 0 auto;
  }

  header{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  h1{
    font-weight: bold;
    margin-bottom: 25px;
    font-size: 70px;
    
  }

  header button{
    border: none;
    padding: 10px;
    width: 50px;
    height: 50px;
    cursor: pointer;
    background-color: rgb(21, 20, 20);
    border-radius: 100%;
    color:white;
    font-size: 20px;
  }

  .card{
    width: 225px;
    height: 225px;
    background-color: rgb(237, 182, 44);
    padding: 10px;
    border-radius: 15px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-bottom: 20px;
    margin-right: 6px;
  }

  .date{
    font-size: 12.5px;
    font-weight: bold;
  }

  .cards-container{
    display: flex;
    flex-wrap: wrap;
  }

  .main-text{
    font-size: 14px;
  }

  .overlay{
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.77);
    z-index: 10;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .modal{
    width: 750px;
    border-radius: 10px;
    background-color: white;
    padding: 30px;
    position: relative;
    display: flex;
    flex-direction: column;
  }

  .modal button{
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

  .modal .close{
    background-color: rgb(193, 15, 15);
    margin-top: 7px;
  }
</style>