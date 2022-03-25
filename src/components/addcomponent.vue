<template>
    <button class="btn btn-success w-100" data-bs-toggle="modal" data-bs-target="#addmodal">Add new student</button>
   <div class="modal fade" id="addmodal" data-bs-backdrop="static" data-bs-keyboard="false">
       <div class="modal-dialog modal-dialog-centered">
           <div class="modal-content">
               <div class="modal-header">
                   <h4 class="text-center">Add new student</h4>
               </div>
               <div class="modal-body">
                   <input  class="form-control my-2" type="text" placeholder="ID" v-model="stdid">
                   <input class="form-control my-2" type="text" placeholder="Name" v-model="stdname">
                   <input class="form-control my-2" type="text" placeholder="City" v-model="stdcity">
               </div>
               <div class="modal-footer">
                   <button class="btn btn-success" data-bs-dismiss="modal" @click="senddata">
                       Add 
                       </button>
                       <button class="btn btn-danger" data-bs-dismiss="modal">
                            Cancel 
                       </button>
               </div>
           </div>
       </div>
   </div>
</template>
<script>
export default ({
    data() {
        return{
            stdid: '',
            stdname:'',
            stdcity:''

        }
        
    },
    methods: {
        senddata() {
            let userinput = {id:this.stdid,Name:this.stdname, city:this.stdcity};
                      // console.log(userinput);

          this.$emit('newstudentadded',userinput);
            
        }

    }
})
</script>