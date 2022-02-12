<template>
  <header>
    <h1>ระบบจัดการข้อมูลพนักงาน</h1>
  </header>
  <FormComponent @save="insertEmployee" />
  <section class="employee-content" v-if="employee.length > 0">
    <h2>ข้อมูลพนักงาน</h2>
    <ListData :employee="employee" />
  </section>
</template>

<script>
    import ListData from './components/ListData.vue'
    import FormComponent from './components/FormComponent.vue'
    export default{
      name: "app",
      components: {
        ListData, FormComponent
      },
      data(){
        return {
          employee: []
        }
      },
      methods:{
        insertEmployee(data){
          this.employee.push(data)
        }
      }

    }

</script>

<style>
*{
  box-sizing: border-box;
}
body{
  margin: 0;
}
header{
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  background-color: salmon;
  color: #FFF;
  text-align: center;
}

.employee-content{
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
}

.employee-content h2{
  font-size: 2rem;
  border-bottom: 4px solid #CCC;
  color: slateblue;
  margin: 0 0 1rem 0;
}
</style>
