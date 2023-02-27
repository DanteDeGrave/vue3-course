<template>
  <div class="navbar">
    <div class="navbar__title" @click="$router.push('/')">Vue 3</div>
    <div class="navbar__btns">
      <my-button @click="$router.push('/posts')">Посты</my-button>
      <my-button @click="$router.push('/store')">Посты из стора</my-button>
      <my-button @click="$router.push('/composition')">Посты c Composition Api</my-button>
      <my-button @click="$router.push('/about')">О приложении</my-button>
    </div>
  </div>
</template>

<script>

export default {
  name: "Navbar",
}
</script>

<style scoped>
.navbar {
  height: 50px;
  background-color: lightgray;
  box-shadow: 2px 2px 4px gray;
  display: flex;
  align-items: center;
  padding: 0 15px;
  justify-content: space-between;
}

.navbar__title {
  color: teal;
  font-weight: 700;
  font-size: 24px;
  cursor: pointer;
}

.navbar__btns {
  display: flex;
  gap: 12px;
}
</style>