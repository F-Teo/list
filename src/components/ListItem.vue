<template>
    <li class="flex mx-5 my-2.5 overflow-auto">
    <span class="w-12 text-blue-400">
      {{ list.index }}
    </span>
    <span class="w-full text-blue-400">
      {{ list.label }}
    </span>
    <span class="w-8 text-blue-200">
      {{ list.value }}%
    </span>
  </li>
</template>

<script>

export default {
  props: {
    list: {
      type: Object,
      required: true
    }
  },
}
</script>

<style scoped>
li {
  display: flex;
  padding: 5px 15px;
  position: relative;
}
li:hover {
  border-radius: 5px;
  background: #234EA3;
  box-shadow: 0 2px 3px #000;
}

li:hover::after {
  content: '\2022';
  position: absolute;
  top: 50%;
  right: 15%;
  transform: translateY(-50%);
  color: #00B3CB;
  box-shadow: px 0px 4px #00B3CB;
}
li:active {
  background-color: #032A75;
}

li:hover span{
  color: #8CC0F1;
}
li:active span{
  color: #7EB5E9;
}
li:hover span:last-child {
  color: #ADEBFF;
}
</style>