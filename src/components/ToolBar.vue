<template>
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.15.2/css/all.css" integrity="sha384-qzVjOd3JSuM7pe8IyYTc0T9g/+TtTn0mw0g4ZO6Y7pZd3oGwTJp8Fh01PYY" crossorigin="anonymous">
  <div class="header">
    <i class="fa fa-bars menu-icon" @click="menuOpen = !menuOpen"></i>
    <div class="title">Welcome</div>
    <div class="header-left" :class="{ 'active': menuOpen }">
      <a href="#" class="button-left">Home</a>
      <a href="#" class="button-left">Login</a>
      <a href="#" class="button-left">SignUp</a>
    </div>
    <div class="header-right" :class="{ 'active': menuOpen }">
      <a href="#" class="button-right ">Home</a>
      <a href="#" class="button-right">Login</a>
      <a href="#" class="button-right">SignUp</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuOpen: false,
    };
  },
};
</script>

<style>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px;
}

.title {
  font-size: 24px;
  font-weight: bold;
  font-family: "Open Sans", sans-serif;
  margin-left: 10px;
}

.header-left,
.header-right {
  display: flex;
  align-items: center;
}

.header-right {
  display: none;
}

.button-left,
.button-right {
  font-family: "Open Sans", sans-serif;
  font-size: 14px;
  color: black;
  border: none;
  border-radius: 20px;
  padding: 8px 15px;
  font-weight: 600;
  margin-right: 4px;
  text-decoration: none;
}

.button-left:hover,
.button-right:hover {
  background-color: rgb(194, 131, 131);
}

.button-left.active,
.button-right.active {
  background-color: rgb(18, 15, 180);
}

.search-icon {
  cursor: pointer;
}

.menu-icon {
  cursor: pointer;
  margin-left: 10px;
}

@media only screen and (max-width: 768px) {
  .header {
    flex-direction: column;
    padding: 0;
  }

  .title {
    margin: 10px 0;
  }

  .header-left {
    display: none;
  }

  .header-right {
    display: none;
    flex-direction: column;
    align-items: center;
  }

  .header-right.active {
    display: flex;
  }

  .menu-icon {
    margin-left: 0;
  }
  
  .button-left,
  .button-right {
    display: block;
    margin: 10px 0;
  }
}
</style>