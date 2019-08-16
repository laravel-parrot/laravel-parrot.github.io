---
title: this is title
description: this is description
author: kamal
---

# about 

## one 

### two

laravel parrot is a laravel module based

# use

## use 2

* test 
* test 2
* test 3

---

* [code4mk](https://code4mk.org)

```php 
function combineLinearArray( $arrayToSmush, $evenItemIsKey = true ) {
    if ( ( count($arrayToSmush) % 2 ) !== 0 ) {
        throw new Exception( "This array cannot be combined because it has an odd number of values" );
    }
    $evens = $odds = array();
    // Separate even and odd values
    for ($i = 0, $c = count($arrayToSmush); $i < $c; $i += 2) {
        $evens[] = $arrayToSmush[$i];
        $odds[] = $arrayToSmush[$i+1];
    }
    // Combine them and return
    return ( $evenItemIsKey ) ? array_combine($evens, $odds) : array_combine($odds, $evens);
}

```


```html 
<!-- test.vue -->
<template>
  <ul>
    <li v-for="todo in todos">
      <input type="checkbox" :checked="todo.done" @change="toggle(todo)">
      <span :class="{ done: todo.done }">{{ todo.text }}</span>
    </li>
    <li><input placeholder="What needs to be done?" @keyup.enter="addTodo"></li>
  </ul>
</template>

<script>
import { mapMutations } from 'vuex'

export default {
  computed: {
    todos () {
      return this.$store.state.todos.list
    }
  },
  methods: {
    addTodo (e) {
      this.$store.commit('todos/add', e.target.value)
      e.target.value = ''
    },
    ...mapMutations({
      toggle: 'todos/toggle'
    })
  }
}
</script>

<style>
.done {
  text-decoration: line-through;
}
</style>
```

```ruby
class Palindrome::Controller

  def initialize(service, persistence)
    @service = service
    @persistence = persistence
  end

  def check(word)
    [{:word=>word, :palindrome=>@service.palindrome?(word)}, :show]
  end

  def list
    [{:words=>@persistence.list}, :list]
  end

end
```
