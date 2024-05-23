<template>
    <div>
        {{  title }}
        <p>  {{ isme }} </p>
        <button @click="dohyeon">click</button>
    </div>
</template>

<script>

export default 
{
    name: 'DohyeonComponent',

    props: 
    {
        title:
        {
            type: String,
            required: true,
        }  
    },

    data() {
        return {
            isme: '이도영',
        }
    },

    methods: {
        dohyeon() {
            this.isme = '나는 이도현!! 이다!!!!';
        }
    }
    
}
</script>

<style scoped>

</style>