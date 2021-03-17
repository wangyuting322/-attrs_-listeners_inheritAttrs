<script>
import lastChild from './LastChild.vue'
export default {
  name: 'LastChild',
  props: {
    msg2: String
  },
  // inheritAttrs: false,
  components: {
    lastChild
  },
  render () {
    console.log(this.$attrs);
    return (
      <div class="grand-child">
        ----------
        <div>
          msg2:{this.msg2}
        </div>
        <last-child {...{
          attrs: {
            ...this.$attrs
          },
          on: {
            ...this.$listeners
          }
        }}></last-child>
      </div>
    )
  }
}
</script>


