# Basic Types - DRAFT WORK IN PROGRESS
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

Have a go at trying to declare a number like we did in our first example, got it?  You should have typed something like this"

```
mynumber := 23
```

Now if you look closely you can see that we have not used speech marks this time, if you had declared your variable like this:

```
mynumber := "23"
```

You would have created a string as the compiler is using the speech marks present to infer the type as string not as a number.  Let's look at some simple maths, if we would like to add two numbers we can do something like this:

```
mynumber1 := 7
mynumber2 := 16

mynumber3 := mynumber1 + mynumber2
```

So what if we had used speech marks?

```
mynumber1 := "7"
mynumber2 := "16"

mynumber3 := mynumber1 + mynumber2
```

What do you think mynumber3 would equal now still 23?
It would in fact equal "716" as we are no longer adding two numbers but joining two strings, ok, one last example to illustrate types.

The benefit of type safety is to save you from making simple mistakes, if you attempt to either assign an integer to a string variable or attempt to add a string and an integer then the compiler will tell you that this is invalid take a look at this example.

```
mynumber := 7
mynumber = "16"
```

This would not be allowed as you can not assign a string to a variable which has been declared as an integer.

```
mynumber1 := 7
mynumber2 := "16"

mynumber3 := mynumber1 + mynumber2
```

This is also invalid and the compiler will complain about this before you end up with a difficult bug to find when running your application.

## Floating point numbers
Integers are useful but the world is not always represented by whole numbers, what about currency we often use decimal places to represent currency and what about when we divide two numbers which would ordinarily produce a remainder.  If we use integers for the following example what do you think the outcome will be?

```
myint1 := 3
myint2 := 2

myint3 := myint1 / myint2
```

If you guessed *1.5* then this is the wrong answer as an integer has no capability for representing decimal places the actual answer would be *1*.  Now in mathematics we are told to round up if the reminder is .5 or greater however when we use integers for division like this we are not rounding the value we are stripping the remainder completely.  To solve this problem many programming languages have a special type called `float` which stands for a floating point number.  In Go we can create a floating point number like this:

```
myfloat := 1.5
```

So if we have a float what if we did something like the below example, what do you think the value of myfloat3 will be?

```
myfloat1 := 1.5
myfloat2 := 2

myfloat3 := myfloat1 * myfloat2
```

If you guessed *3* then again this unfortunately is the wrong answer, Go will not allow you to multiply these two numbers in the same way as it would not allow you to add a string and an integer from our earlier example as whilst they are both numbers they are not the same type.  *myfloat1* is actually a `float64` while *myfloat2* is actually an `int`.  If we change the example to be written like the below then what do you think the output will be?

```
myfloat1 := 1.5
myfloat2 := 2.0

myfloat3 := myfloat1 * myfloat2
```

If you answered *3* then this time you are correct as both numbers are both type float64.

So why do we not just make all numbers floating point?
Well we again need to think about efficiency to store a float in memory it is actually stored not explictly as ones and zeros but in parts which allow the calculation of the number, therefore for a 32 bit floating point number you loose 8 bits to store the exponent.  Now in additon loosing storage we also need to consider the problem that storing an whole number as a float can actually introduce rounding problems when you are multiplying numbers.   *Going to park this as I am not sure the explanation is helping*

## Boolean
A boolean or bool value is just a fancy name for something which is either true or false, in Go lang we can create a boolean with the following syntax.

```
mybool := true
var myfalsebool bool
```

If you create a boolean value and do not associate it a value then its default is *false* when creating boolean values then we need to remember to not use speech marks or you will create a string and as we learned when looking at integers "1" is not equal to 1 therefore "true" is not equal to true.

## Declaring variable
Now just to keep you on your toes there are three different ways we can declare a vairable in go the first is the one we have been using so far.

`variable := "some value"`

The key thing to note here is the special operator `:=` the `:` part of this operator means *create* the second the `=` is assign so the full operator is *create and assign*

We do not need to explicitly specify a type as the compiler infers this from the assignment for example.

```
myInteger := 1 // creates an int since the assigned value is a number
myString := "a string" // creates a string since the assigned value is a string
```

This is all fairly simple but what when you want to create a variable but not assign any value? In this case we can use the `var` keyword and this works like so.

```
var myString string
myString = "something"
```

Now note because we are not assigning a value we need to explicitly state the type.  All variables must have a type and this is why we must state it if we use this method.
In the second line we are assigning a value using the `=` operator, if we try to use the `:=` operator to *create and assign* to an existing variable the compiler will complain as it can not create what already exists.

We can also use the var operator to create a variable and assign it in one go using the below syntax.

```
var myString = "Something"
```

Why would you want to do this?  Whilst this is valid syntax inside of a function the use is mainly restricted to when you wish to declare a package level variable outside of a function like this example.

```
var myString = "Something"

func PrintMyString() {
  fmt.Println(myString) // prints Something to the output
}
```

## Default Values
Lets take a look at some other default values, create an instance of an integer and a string variable and do not assign it a value.  What do you think the default will be?

```
var mystring string // = ""
var myinteger int // = 0
var mybool bool // = false
```

Types always have a default value there is an exception for the special type interface and we will look at that later.  

## Constants
These are special variables that can never change.