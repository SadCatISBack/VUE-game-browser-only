<template>
  <h1>{{ msg }}</h1>
 <div class="page">
   <div class="login">
    <label>User name:</label>
      <input required v-model="username" type="text" placeholder="login"/>
    <label>Password:</label>
    <input required v-model="password" type="password" placeholder="passwor"/>
  <button>Sing In</button>
  </div>
   <div class="singup">
     <label>User name:</label>
     <input required v-model="username" type="text" placeholder="login"/>
     <label>E-mail:</label>
     <input required v-model="username" type="text" placeholder="login"/>
     <label>Password:</label>
     <input required v-model="password" type="password" placeholder="passwor"/>
     <button>Sing Up</button>
   </div>
 </div>
</template>

<script>
export default {
  name: 'RegLog',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.page{
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.login, .singup{
  margin: 100px;

  min-width: 300px;
  min-height: 200px;

  color: darkgreen;

  display: flex;
  flex-direction: column;
  align-content: center;
  justify-content: start;
}




button {
  position: relative;
  display: inline-block;
  color: #777674;
  font-weight: bold;
  text-decoration: none;
  text-shadow: rgba(255,255,255,.5) 1px 1px, rgba(100,100,100,.3) 3px 7px 3px;
  user-select: none;
  padding: 1em 2em;
  outline: none;
  border-radius: 3px / 100%;
  background-image:
      linear-gradient(45deg, rgba(255,255,255,.0) 30%, rgba(255,255,255,.8), rgba(255,255,255,.0) 70%),
      linear-gradient(to right, rgba(255,255,255,1), rgba(255,255,255,0) 20%, rgba(255,255,255,0) 90%, rgba(255,255,255,.3)),
      linear-gradient(to right, rgba(125,125,125,1), rgba(255,255,255,.9) 45%, rgba(125,125,125,.5)),
      linear-gradient(to right, rgba(125,125,125,1), rgba(255,255,255,.9) 45%, rgba(125,125,125,.5)),
      linear-gradient(to right, rgba(223,190,170,1), rgba(255,255,255,.9) 45%, rgba(223,190,170,.5)),
      linear-gradient(to right, rgba(223,190,170,1), rgba(255,255,255,.9) 45%, rgba(223,190,170,.5));
  background-repeat: no-repeat;
  background-size: 200% 100%, auto, 100% 2px, 100% 2px, 100% 1px, 100% 1px;
  background-position: 200% 0, 0 0, 0 0, 0 100%, 0 4px, 0 calc(100% - 4px);
  box-shadow: rgba(0,0,0,.5) 3px 10px 10px -10px;
}
button:hover {
  transition: .5s linear;
  background-position: -200% 0, 0 0, 0 0, 0 100%, 0 4px, 0 calc(100% - 4px);
}
button:active {
  top: 1px;
}


</style>
