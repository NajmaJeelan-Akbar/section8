<template>
    <div class="component">
        <h1>The User Component</h1>
        <p>I'm an awesome User!</p>
        <button @click="ChangeName">ChangeMyname</button>
        <p>name is {{name}}</p>
        <p>age is {{age}}</p>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-6">
                <app-user-detail v-bind:name="name"
                @nameWasReset="name=$event"
                 :resetFn="resetName"
                 :userAge="age"></app-user-detail>
            </div>
            <div class="col-xs-12 col-sm-6">
    
                <app-user-edit  :userAge="age"
                @ageWasEdited="age = $event">
                 </app-user-edit>
            </div>
        </div>
    </div>
</template>

<script>
    import UserDetail from './UserDetail.vue';
    import UserEdit from './UserEdit.vue';

    export default {
      data:function(){
        return{
          name:'Najma',
          age:'27'
        }
      },
      methods:{
        ChangeName(){
          this.name='Vasiya';
        },
        resetName(){
          this.name='Najma';
        }
      },
        components: {
            appUserDetail: UserDetail,
            appUserEdit: UserEdit
        }
    }
</script>

<style scoped>
    div {
        background-color: lightblue;
    }
</style>
