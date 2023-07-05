<template>
    <div class="container">
        <div class="box">
            <h2>🤸‍♂️BESHIFY APP🤸‍♂️</h2>
            <hr>
            <div class="forms">
                <input type="text" name="" id="" placeholder="Add Text...." v-model="input">
            <button @click="process">Convert</button>
            <textarea name="" id="" placeholder="Output...." column=30 row=30>{{ output }}</textarea>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    data(){
        return{
            input:"",
            output:""
        }
    },
    methods:{
        
        process(){
            let value = this.input;
            let out = value.replaceAll(" ","🤸‍♂️")
           this.output=out
            
        }
    }
    
}
</script>


<style scoped>
.container{
    width: 100%;
    height: 100%;
    display:flex; 
    justify-content:center;
    align-items:center;
    text-align:center;
}

.box{
    width: 30%;
    height: 70%;
    background: whitesmoke;
    border-radius:10px;
}

h2{
    text-align:center;
}

hr{
    width: 70%;
    text-align:center;
}

.forms{
    display:flex;
    flex-direction:column;
    margin-top:30px;
    padding: 0 40px;
    gap:20px;
    justify-content:center;
}


input[type="text"]{
    border: none;
font-size: 1.5em;
font-family: sans-serif;
padding: 10px 15px;
background: whitesmoke;
border-bottom:1px solid  teal;
}

button{
    background: rgb(255, 46, 99);
    color: white;
    font-size: 1.25em;
}
textarea{
    border: none;
font-size: 1.5em;
font-family: sans-serif;
padding: 10px 15px;
background: whitesmoke;
border-bottom:1px solid  teal;
height: 180px;
}

@media (max-width:450px){
.box{
    width: 60%;
    height: 70%;
    
}

input[type="text"]{
font-size: 1.25em;
padding: 8px 10px;
}

button{
    background: rgb(255, 46, 99);
    color: white;
    font-size: 1.15em;
}
textarea{
font-size: 1.25em;
padding: 8px 10px;
height: 130px;
}

}
</style>