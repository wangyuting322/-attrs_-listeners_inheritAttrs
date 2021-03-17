<script>
import child from './components/Child.vue'

export default {
  name: 'App',
  components: {
    child
  },
  mounted () {
    console.log(this.$attrs);
  },
  render () {
    return (
      <div id="app">
        <child msg="Welcome to Your Vue.js App" msg2='ddd' msg3='sfsdf' onClick={(e) => { console.log(e); }} />
      </div>
    )
  }
}
</script>

