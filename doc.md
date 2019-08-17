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
    * one 
    * two
    * there
        * four
* test 2
* test 3

1. First ordered list item
2. Another item


~ `kamal is here` ok
// Lab2.java Starter File

import java.io.*; // BufferedReader
import java.util.*; // Scanner

public class Lab2
{
  public static void main (String args[]) throws Exception // i.e. the input file you put on cmd line is not in directory
  {
    // ALWAYS TEST FIRST TO VERIFY USER PUT REQUIRED INPUT FILE NAME ON THE COMMAND LINE
    if (args.length < 1 )
    {
      System.out.println("\nusage: C:\\> java Lab2 <input filename>\n\n"); // i.e. C:\> java Lab2 input.txt
      System.exit(0);
    }
    BufferedReader infile = new BufferedReader (new FileReader( args[0] )); // we read our text file line by line
    int lineNum=0;
    while( infile.ready() )
    {
      String line = toAlphaLowerCase(infile.readLine());
      if ( isPalindrome( line ) )
      System.out.format("<%s> IS palindrome.\n",line);
      else
      System.out.format("<%s> NOT palindrome.\n",line);
    }
  } // END MAIN
  
  // ******* MODIFY NOTHING ABOVE  THIS   LINE YOU FILL IN THE METHODS BELOW *******
  // RETURNS A STRING WITH ALL NON ALPHABETIC CHARS REMOVED. ALL REMAINING ARE ALPHAS CONVERTED TO LOWER CASE
  // "Madam I'm Adam" returns "madamimadam" which is now ready for a simple palindromic test
  // To test whether a char is alpha i.e. letter of the alphabet
  // read this ==> https://docs.oracle.com/javase/tutorial/i18n/text/charintro.html
  static String toAlphaLowerCase( String s )
  {
    String clean = "";
    for (int i = 0; i < s.length(); i++) {
      
      if (Character.isLetter(s.charAt(i)) == true)
      clean += Character.toLowerCase(s.charAt(i));
    }
    return clean; // (just to make it compile) YOU CHANGE AS NEEDED
  }
  // RETURNs true if and only if the string passed in is a palindrome
  static boolean isPalindrome( String s )
  {
    if (s.equals("") || s == null) {
      return true;
    }
    
    
    for (int i = 0; i < s.length() / 2; i++) {
      if (s.charAt(s.length() - 1 - i) != s.charAt(i)) {
        return false;
      }
    }
    return true; // (just to make it compile) YOU CHANGE AS NEEDED
  }
} // END LAB2 CLASS
---

* [code4mk](https://code4mk.org)

```java 

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
