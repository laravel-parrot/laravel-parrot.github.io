---
title: this is title
description: this is description
author: kamal
---

# about 

## one 

### two

laravel parrot is a laravel module based

<div class="alert alert-primary" role="alert">
  A simple primary alert—check it out!
</div>



# use

<table class="table table-dark">
  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td>Larry</td>
      <td>the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>
</table>

## use 2


| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |




* test 
    * one 
    * two
    * there
        * four
* test 2
* test 3

1. First ordered list item
2. Another item


~ `kamal is here` ok



* [code4mk](https://code4mk.org)


```java 
 public class Palindrome {

	public static void main(String[] args) {
		System.out.println(isPalindrome("amor roma"));
		System.out.println(isPalindrome("Was it a car or a cat I saw?"));
	}

	public static Boolean isPalindrome(String text) {
		StringBuilder builder = new StringBuilder();
		for (char c : text.toCharArray()) {
			if (Character.isAlphabetic(c)) {
				builder.append(Character.toLowerCase(c));
			}
		}

		text = builder.toString();
		int len = text.length();
		
		for (int i = 0; i < len / 2; ++i) {
			if (text.charAt(i) != text.charAt(len - i - 1)) {
				return false;
			}
		}
		return true;
	}
}
 
```


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
