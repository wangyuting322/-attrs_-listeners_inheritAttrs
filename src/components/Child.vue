<script>
import grandChild from './GrandChild.vue'
export default {
  name: 'Child',
  props: {
    msg: String
  },
  inheritAttrs: false,
  components: {
    grandChild
  },
  render () {
    console.log(this.$attrs);
    return (
      <div class="child" >
        ----------
        <div div >
          msg: {this.msg}
        </div >
        <grand-child {...{
          attrs: {
            ...this.$attrs
          },
          on: {
            ...this.$listeners
          }
        }}></grand-child>
      </div >
    )
  }
}
</script>


