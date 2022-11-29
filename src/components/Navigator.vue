<script>
export default {
  name: "src-componentes-navigator-vue",
  props: ['mensaje','termino'],

  mounted() {
  },

  data() {
    return {
      isHardNav: true,      
      colorCount:6,                  
    };
  },
  methods: {
    restart() {
        this.$emit("restart");
    },
    changeHard() {
      if (!this.isHardNav) {
        this.isHardNav = true;              
        this.colorCount=6
        this.$emit("is-hard-navigator", this.isHardNav);
        this.$emit("color-count", this.colorCount);
        this.$emit("restart");
      }
    },
    changeEasy() {
      if (this.isHardNav) {
        this.isHardNav = false;              
        this.colorCount=3
        this.$emit("is-hard-navigator", this.isHardNav);
        this.$emit("color-count", this.colorCount);
        this.$emit("restart");
      }
    },    
  },
  computed: {},
};
</script>

<style scoped lang="css" >
.src-componentes-navigator-vue {
}

</style>