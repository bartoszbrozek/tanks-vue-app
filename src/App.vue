<template>
    <div id="app">
        <div class="d-flex flex-column flex-md-row align-items-center p-3 px-md-4 mb-3 bg-white border-bottom shadow-sm">
            <h5 class="my-0 mr-md-auto font-weight-normal">Tanks</h5>
            <nav class="my-2 my-md-0 mr-md-3">
                <router-link to="/">Tanks </router-link>
                <router-link to="/about">About</router-link>
            </nav>
        </div>

        <router-view/>
    </div>
</template>

<style>
    @import url('https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css');
</style>
