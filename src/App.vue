<template>
  <main>
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

  button{
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
</style>