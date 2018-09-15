<template>
    <div class="home">
        <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
            <h1 class="display-4">Tanks are awesome!</h1>
            <p class="lead">These steel beasts are built to be a dangerous threat for your enemy forces. Do not
                underestimate them!</p>
            <p class="lead">Add your own tank... now!</p>
        </div>

        <div class="container">
            <div class="pricing-header px-3 py-3 pt-md-5 pb-md-4 mx-auto text-center">
            <TankCards></TankCards>
            </div>

            <footer class="pt-4 my-md-5 pt-md-5 border-top">
                <div class="row">
                    <div class="col-6 col-md">
                        <h5>Features</h5>
                        <ul class="list-unstyled text-small">
                            <li><a class="text-muted" href="#">Tanks</a></li>

                        </ul>
                    </div>
                    <div class="col-6 col-md">
                        <h5>Resources</h5>
                        <ul class="list-unstyled text-small">
                            <li><a class="text-muted" href="#">More tanks</a></li>

                        </ul>
                    </div>
                    <div class="col-6 col-md">
                        <h5>About</h5>
                        <ul class="list-unstyled text-small">
                            <li><a class="text-muted" href="#">Even more tanks</a></li>

                        </ul>
                    </div>
                </div>
            </footer>
        </div>
    </div>
</template>

<script>
  import TankCards from '../components/TankCards.vue'

  export default {
    name: 'home',
    components: {
      TankCards
    }
  }
</script>
