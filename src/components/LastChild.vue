<script>
export default {
  name: 'LastChild',
  props: {
    msg3: String
  },
  // inheritAttrs: false,
  methods: {
    handleClick (e) {
      this.$emit('click', e)
    }
  },
  render () {
    console.log(this.$attrs);
    return (
      <div class="grand-child">
        -----------
        <div>
          msg3:{this.msg3}
        </div>
        <button onClick={(...args) => { this.handleClick(...args) }}>点我</button>
      </div>
    )
  }
}
</script>


