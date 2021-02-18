<template>
  <div class="body">
    <left></left>
    <body-middle></body-middle>
    <right></right>
  </div>
</template>

<script>
import BodyMiddle from '../../../components/BodyMiddle.vue';
import Left from '../../../components/Left.vue';
import Right from '../../../components/Right.vue';

export default {
  data() {
    return {};
  },
  created() {},
  computed: {},
  methods: {},
  components:{Left,  BodyMiddle, Right}
};

</script>

<style scoped>
.body {
  display: flex;
  margin: 0px auto;
  width: 1880px;
}
</style>
