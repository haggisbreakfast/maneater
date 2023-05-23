<template>
  <div class="content-window drop-shadow">
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="(item, index) in list" :key="index">
        <a :href="item.link">
          <span>{{ item.name }}</span>
        </a>
        <span>{{ item.venue }}</span>
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'ContentWindow',
  props: {
    title: String,
    msg: String,
    list: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.content-window {
  margin: 2rem;
  background: #FDF5BF;
  border: 8px solid #5397CF;
  animation-name: blinking;
  animation-duration: 1s;
  animation-iteration-count: 100;
  padding: 1rem;
  @media (min-width: 680px) {
    width: 50%;
  }
}
@keyframes blinking {
  50% {
    border-color: #ffcd5f;
  }
}
h1 {
color:#5397CF;
font-weight: bold;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: flex;
  flex-direction: column;
  color: #D27774;
  margin: 1rem 0;
}
a {
  color: #D27774;
  font-size: 24px;
}
span {
}
</style>
