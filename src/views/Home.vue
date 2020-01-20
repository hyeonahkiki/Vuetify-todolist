<template>
  <div class="home">
    <v-container>
      <v-row>
        <Todo/>
        <!-- v-spacer 둘 사이의 공간을 띄울때 사용하는 태그 -->
        <v-spacer></v-spacer>
        <Done/>
      </v-row>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import Todo from '../components/Todo'
import Done from '../components/Done'


export default {
  name: 'home',
  components: {
    Todo,
    Done,
  }
}
</script>
