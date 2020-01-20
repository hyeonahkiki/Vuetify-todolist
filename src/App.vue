<template>
  <div>
    <!-- color 찾아서 #붙은거 써주면 됨 -->
    <v-app-bar
      color="#BBDEFB"
    >
    
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Todo List</v-toolbar-title>

      <v-spacer></v-spacer>
    
        <TodoInput/>
        <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu
        left
        bottom
      >
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on">
            <v-icon>mdi-dots-vertical</v-icon>
          </v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="n in 5"
            :key="n"
            @click="() => {}"
          >
            <v-list-item-title>Option {{ n }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
    <!-- 예전에 block / endblock이랑 같은 느낌 -->
    <router-view/>
  </div>
</template>

<script>
import TodoInput from './components/TodoInput'

export default {
  name: 'App',
  components: {
    TodoInput
  },
};
</script>
