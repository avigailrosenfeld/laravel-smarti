<template>
    <div class="container"> 
        <nav class="navbar navbar-expand-lg navbar-light bg-light">
            <div class="collapse navbar-collapse">
                <div class="navbar-nav">
                    <router-link to="/" class="nav-item nav-link">Beers List</router-link>
                    <router-link to="/create" class="nav-item nav-link">Create New Beer</router-link>
<div class="container">
    <div class="row justify-content-center">
         
                <div class="card-header text-center">Search</div>
                  <autocomplete-component></autocomplete-component>
                 
    </div>
</div>
                </div>
            </div>
        </nav>

        <router-view> </router-view>
    </div>
</template>
 
<script>
    export default {}
</script>
