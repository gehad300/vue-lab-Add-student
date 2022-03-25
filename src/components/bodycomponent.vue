<template>
<addcomponent @newstudentadded="testeventraised"/>
  <table class="table table-bordered table-striped">

    <thead>
      <tr>
        <th>ID</th>
        <th>Name</th>
        <th>City</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="student in students" :key="student.id">
        <td>{{ student.id }}</td>
        <td>{{ student.Name }}</td>
        <td>{{ student.city }}</td>
      </tr>
    </tbody>
    <tfoot>
      <tr>
        <th colspan="3">Total no of students :{{students.length}}</th>
      </tr>
    </tfoot>
  </table>
</template>

<script>
import students from "../students";
import addcomponent from "./addcomponent.vue"
export default {
  data() {
    return {
      students: students,
    }
  },
  components:{
    addcomponent
  },
  methods:{
    testeventraised(data){
    // console.log("hello from body : "+data);
    this.students.push(data);

    }
  }
};
</script>