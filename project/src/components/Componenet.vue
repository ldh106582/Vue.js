<script scope>
export default {
    props: {
        title: {
            type: String,
            required: true,
        }
    },

    methods: {
        updateName(){
            this.name = "이렇게 연습하면 되는건가?";
        }
    }
}
</script>