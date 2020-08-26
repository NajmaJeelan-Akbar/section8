<template>
    <div class="component">
        <h3>You may view the User Details here</h3>
        <p>Many Details</p>
        <p>User Name: {{name}}</p>
        <p>User Age: {{ userAge }}</p>
        <button @click="resetName">ResetName</button>
        <button @click="resetFn()">ResetName</button>
        
    </div>

</template>

<script>
export default{
  props:{
      name:{
          type:String
      },
      resetFn:Function,
      userAge:Number
  },
  methods:{
      switchName(){
          return this.name.split("").reverse().join("");
      },
      resetName(){
          this.name='Najma';
          this.$emit('nameWasReset',this.name);
      },
      
  }
}
</script>

<style scoped>
    div {
        background-color: lightcoral;
    }
</style>
