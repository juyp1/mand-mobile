<template>
  <div class="md-example-child md-example-child-switch md-example-child-switch-0">
    <md-switch
      v-model="isActive"
      @change="handler('switch0', isActive, $event)"
    ></md-switch>
  </div>
</template>

<script>
import {Switch} from 'mand-mobile'

export default {
  name: 'switch-demo',
  /* DELETE */
  title: '开启状态',
  /* DELETE */
  components: {
    [Switch.name]: Switch,
  },
  data() {
    return {
      isActive: true,
    }
  },
  methods: {
    handler(name, active) {
      console.log(`Status of switch ${name} is ${active ? 'active' : 'inactive'}`)
    },
  },
}

</script>