<template>
    <div>
      <h1 :class="{'tittle': true, 'tittle-home': isHome}">
        Curso Vue 3
      </h1>
      <p :class="pClass">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quas aperiam cum dolorem vitae, deleniti consequatur soluta nulla voluptas quisquam ipsum quam cupiditate, placeat repellat unde rem non tenetur blanditiis reprehenderit.
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore, dolorum. Beatae quibusdam dolorem minima fuga maxime facilis excepturi saepe impedit architecto hic non ipsum eius molestiae reiciendis, exercitationem deleniti ab!
      </p>

      <p :style="StyleClass">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores pariatur laboriosam corporis alias repellendus veniam numquam soluta dolores, facere quaerat officia nemo perspiciatis tenetur vero nisi porro sequi, similique deserunt.
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Minima ut explicabo magni, delectus numquam asperiores sed illo excepturi rerum alias blanditiis impedit quam neque? Praesentium non voluptatum saepe blanditiis! Perspiciatis?
      </p>
    </div>
  
    <div v-for="obj in todos" 
      v-bind:key="obj.id">

            {{ obj.title }}

            <img 
    v-if="obj.imgSRC"
    :src="obj.imgSRC" 
    alt="">
    </div>

  

</template>


<script>
export default {
  data() {
    return {
      StyleClass: {'color': 'black', 'background-color': 'orange'},
      pClass: ['text', 'text-home'],
      isHome: true,
      ClassVar: 'tittle',
      todos:
      [
        {
          "userId": 1,
          "id": 1,
          "title": "delectus aut autem",
          "completed": false,
          "imgSRC":"../src/assets/image/chopper.PNG",
          
  },
  {
    "userId": 1,
    "id": 2,
    "title": "quis ut nam facilis et officia qui",
    "completed": false,
    "imgSRC":"../src/assets/image/chopper.PNG",
  },
  {
    "userId": 1,
    "id": 3,
    "title": "fugiat veniam minus",
    "completed": false
  },
  {
    "userId": 1,
    "id": 4,
    "title": "et porro tempora",
    "completed": true
  },
  {
    "userId": 1,
    "id": 5,
    "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
    "completed": false
  },
  {
    "userId": 1,
    "id": 6,
    "title": "qui ullam ratione quibusdam voluptatem quia omnis",
    "completed": false
  },
  {
    "userId": 1,
    "id": 7,
    "title": "illo expedita consequatur quia in",
    "completed": false
  },
  {
    "userId": 1,
    "id": 8,
    "title": "quo adipisci enim quam ut ab",
    "completed": true
  }, ]  
    }
  }
}
</script>


<!-- <template>
    <div v-for="obj in todos" 
    v-bind:key="obj.id"
    class="todos-item"
    >
        {{ obj.title }}
    </div>
</template>

<script>

export default {
    data() {
        return {
            todos:
            [
  {
    "userId": 1,
    "id": 1,
    "title": "delectus aut autem",
    "completed": false
  },
  {
    "userId": 1,
    "id": 2,
    "title": "quis ut nam facilis et officia qui",
    "completed": false
  },
  {
    "userId": 1,
    "id": 3,
    "title": "fugiat veniam minus",
    "completed": false
  },
  {
    "userId": 1,
    "id": 4,
    "title": "et porro tempora",
    "completed": true
  },
  {
    "userId": 1,
    "id": 5,
    "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
    "completed": false
  },
  {
    "userId": 1,
    "id": 6,
    "title": "qui ullam ratione quibusdam voluptatem quia omnis",
    "completed": false
  },
  {
    "userId": 1,
    "id": 7,
    "title": "illo expedita consequatur quia in",
    "completed": false
  },
  {
    "userId": 1,
    "id": 8,
    "title": "quo adipisci enim quam ut ab",
    "completed": true
  }, ] 
        }
    }
}


</script> -->

<style>
.tittle {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  font-size: 50px;
}

.tittle-home {
  font-size: 70px;
  color: aqua;
}

.text {
  color: orange;
}
.todos-item {
    background-color: #000;
    margin: 0 0 5px 0;
    padding: 3px 6px;
    color: white;
}

.text-home {
  color: #00e660;
  font-size: 15px;
}
.header {
background-color: burlywood;
color: black;   
text-align: center;
font-family:Arial, Helvetica, sans-serif ;
}
</style>
