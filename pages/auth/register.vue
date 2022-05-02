<template>
<div class="container">
    <div class="col-md-6 offset-md-3">
        <div class="card mt-4">
            <div class="card-header">
                <p>Register Here</p>
            </div>
            <div class="card-body">
                <form @submit.prevent="register">
                    <div class="form-group">
                        <label for="">Name</label>
                        <input v-model="form.name" type="text" class="form-control" placeholder="Enter Name here">
                    </div>
                    <div class="form-group">
                        <label for="">Email</label>
                        <input type="email" v-model="form.email" class="form-control" placeholder="Enter Email here">
                    </div>
                    <div class="form-group">
                        <label for="">Name</label>
                        <input type="password" v-model="form.password" class="form-control" placeholder="Enter Password here">
                    </div>
                    <div class="from-group">
                        <input type="submit" value="Submit" class="btn btn-success w-100">
                    </div>
                </form>
            </div>
        </div>
    </div>
</div>
    
</template>
<script>


export default  {
    data(){
        return {
            form:{
                name:'',
                email:'',
                password:''
            }
        }
    },
    methods:{
        async register(){
            console.log(this.form)
            await this.$axios.post('http://127.0.0.1:8000/api/auth/register',this.form);

            this.$auth.login({data:this.form});
            this.$router.push({name:'index'})
        }
    }
}
</script>
