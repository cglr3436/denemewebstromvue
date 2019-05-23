<template>
    <div class="test" >
        <h1>{{ msg }}</h1>
<!--        <p>{{title}}</p>-->
        <div v-if="showname">
            <p >{{user.adi}}</p>
            <p>{{user.soyadi}}</p>
        </div>

<!--        <p v-text="user.adi"></p>-->
        <button v-on:click="greet">AC / KAPA </button>
    </div>
</template>


<script>
    export default {
        el: '#test',
        name: "TestComponent",
        // props: {
        //     msg: String
        // },
        data() {
            return {
                mgs: "test data",
                title:"hellloo",
                user: {
                    adi:'caglar',
                    soyadi:'kockara'
                }
                ,showname:true
            }

        },

        methods:{
          greet:function () {
              // alert('hello');
              if(this.showname) {
                  this.showname = false;
              }else {
                  this.showname = true;
              }
          }
        }
    }
</script>

<style scoped>
    h3 {
        margin: 40px 0 0;
    }
</style>