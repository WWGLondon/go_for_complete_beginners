# Basic Types
Types in Go are things like numbers, strings, booleans which represent true or false and more complex objects which we will talk about in the next session.

Firstly we are going to take a look at how we can create and assign variables, a variable is an instance of a type.  If you think of a type as a human and a variable as you then you are an instance of human, of course we are all instances of humans and like variables we are all different but be all of the same type.

## Strings

So how do we declare a variable, let's take a look at the string type to see how:


```
  mystring := "Hello World"
```

When dealing with varibles it is sometimes best to read from the right to the left, writing `"Hello World"` in speech marks tells go that we are dealing with a string.  Then we have the special operator `:=`, this is different from just `=` as we are creating and assigning a new varaible with the name `mystring`.

There is another way in which we can declare a variable in go"

``` 
  var mystring string
  mystring = "Hello World"
```

In this example we are using the keyword *var* this tells Go that you would like to declare a new variable, after the name of the variable you will see that we have referenced the type in this case *string*.  When we create varaibles using this format we must include the type as the compiler can not infer the type from the assignment in the first example.

Well that is unless we look at the third way we can declare a variable:

```
  var mystring = "Hello World"
```

Confused yet?  No need to be the most common way we use variables is the first form and this is what you should mainly attempt to use.  The other forms are special case but you will see them in other peoples Go code so it is important to recognise how they work.

## Mention declaring variables outside of functions and draw reference to the above

## Integers
Integers are whole numbers like 1,3,23,23034343 they do not have any decimal places and come in various sizes. 
We have:
* int - which is most likely an alilias for int64
* int8
* int16
* int32
* int64

It is useful but not essential to understand how numbers work in order to realize why we have all of these different kinds.  We need to think about how a computer uses memory, in a computers memory it does not store a number like *23* it actually stores it as a sequence of 0s and 1s called binary.
Memory is made up of bytes and each byte contains 8 bits which are either 0 or 1, so if we look at how we would write our number *23* in binary it would be written like so...

0 0 0 1 0 1 1 1

That is because each bit in a byte represents a value of either 128, 64, 32, 16, 8, 4, 2, 1 . In our example above the number equals 23 because we add up the values of all the bits which are set to 1 so 16 + 4 + 2 + 1 = 23.

Now the reason we have all of these diffent types for a number is because of the amount of memory it uses to store the value.  So an int8 would have a maximum value of 256 which is the sum of all 8 bits, an int16 or 16 bit number would have a maximum value of 65532 which again is the sum of the bits because in a 16 bit number the 9th bit has a value of 256 and the 10th 512 and so on.

Do not worry too much about this and in fact feel free to forget it as most of the time when you are dealing with numbers you will only use int which on a modern computer is a 64 bit number.  It is interesting to know the underlying theory of how that works if you feel the need to liven up a boring dinner party with some interesting geek facts.
