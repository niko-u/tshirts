<template>

<nav class="navbar fixed-top navbar-expand-lg navbar-light " style="background-color: #89cc95;">
  <div class="container-fluid">
    <a class="navbar-brand" href="#" id="title">TSHIRTS</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Gallery</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Artist Portal</a>
        </li>
        <li class="nav-item">

        </li>
      </ul>
            <form class="d-flex">
                <input id="search" class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
            </form>
        <a class="navbar-brand" href="#">
            <img src="../assets/profilepic.png" alt="" width="35" height="35" class="rounded-circle d-inline-block align-text-top" id="profile">
        </a>
    </div>
  </div>
</nav>

    
</template>

<script>

</script>

<style scoped>

.nav-link {
    font-size: 20px;
    font-family: Arial;
    font-style: bold;
}

#profile {
    margin-left: 20px;
}

#title {
    font-size: 25px;
    font-family: Arial;
    font-style: bold;
}


</style>
