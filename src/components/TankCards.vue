<template>

    <div class="TankCards">

        <h2 class="display-4">Add a New Tank</h2>
        <form v-on:submit.prevent="addTank">

            <div class="form-group">
                <label>Name</label>
                <input type="text" class="form-control" v-model="Tank.name">
                <small class="form-text text-muted">Enter tank name</small>

                <label>Price</label>
                <input type="text" class="form-control" v-model="Tank.price">

                <label>Frontal Armor</label>
                <input type="number" class="form-control" v-model="Tank.frontalArmor">

                <label>Rear Armor</label>
                <input type="number" class="form-control" v-model="Tank.rearArmor">

                <label>Side Armor</label>
                <input type="number" class="form-control" v-model="Tank.sideArmor">
            </div>

            <button type="submit" class="btn btn-primary">Add This Epic Destruction Tool</button>
        </form>
        <hr>

        <h2 class="display-4" v-if="tanks.length > 0">Tank List</h2>
        <h2 class="display-4" v-else>You do not have any tanks :<</h2>
        <div class="card-deck mb-3 text-center" v-for="(tank, index) in tanks" :key="index">
            <div class="card mb-6 shadow-sm">
                <div class="card-header">
                    <h4 class="my-0 font-weight-normal">{{ tank.Tank.name }}</h4>
                </div>
                <div class="card-body">
                    <h1 class="card-title pricing-card-title">${{ tank.Tank.price }}
                        <small class="text-muted">/ One Time</small>
                    </h1>
                    <ul class="list-unstyled mt-6 mb-6">
                        <li>Frontal Armor: {{ tank.Tank.frontalArmor }}</li>
                        <li>Rear Armor: {{ tank.Tank.rearArmor }}</li>
                        <li>Side Armor: {{ tank.Tank.sideArmor }}</li>
                    </ul>
                    <button type="button" class="btn btn-lg btn-block btn-outline-primary">Get me now!</button>
                    <button type="button" class="btn btn-lg btn-block btn-outline-danger" @click="removeTank(index)">
                        Remove this tank :(
                    </button>
                </div>
            </div>
        </div>
    </div>

</template>

<script>
  export default {
    name: 'TankCards',
    data () {
      return {
        Tank: {
          name: '',
          frontalArmor: 0,
          rearArmor: 0,
          sideArmor: 0,
          price: 0
        },
        tanks: []
      }
    },
    methods: {
      addTank () {
        this.tanks.push({
          Tank: {
            name: this.Tank.name,
            frontalArmor: this.Tank.frontalArmor,
            rearArmor: this.Tank.rearArmor,
            sideArmor: this.Tank.sideArmor,
            price: this.Tank.price
          }
        })
      },

      editTank (index) {
        this.tanks[index] = this.Tank
      },

      removeTank (index) {
        this.tanks.splice(index, 1)
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
