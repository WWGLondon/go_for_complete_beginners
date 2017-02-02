# Why Go?

Imagine that you're on your first step into coding, this would be the first question to pop in your head, why should I learn Go? why not any other language? Ruby? C++? Java?

The answer is simple, because Go is awesome! but why? Well.. this is what you'll learn through the workshop. (I found this answer quite catchy)

At this point, I'd share a personal story, something like:
- what my background is.
- how I got into coding.
- how my journey with Go started.

Now that people warmed up to the idea, we can actually start introducing what's in the store.

## What is Go?

- Go is a general purposed programming language
  - http://awesome-go.com/ has both list and proof of why it is called a general-purposed programming language.
- It is compiled
  - All programs have to be converted to a form that the computer understands Some languages like Python and Ruby do this as you run the program Other languages like Go require a special step, called compiling.
  - there is no virtual machine, neither interpreter, all in binary and it is super fast.
  - It also compiles in different OS, you can compile it now in your machine and compile it again in a totally different machine and it would work.
- It is concurrent
  - nowadays machine has multiple cores, Go knows how to deal with this, it incorporates concurrency primitives that makes working with today's asynchronous network world.
- It is simple
- It is statically typed
- It has powerful standard library, all in all it is a clean low level language, garbage collected like scripting language, so we don't have to worry too much about memory management, but with the powerful standard library it lets you do a lot of high level programming.
- All those above combined makes working with Go: Fast, Fun & Productive

### A little bit of history

- Google, one of the best Software Engineering firm in the world, hit a wall and created a new language - which is Go.
- It was started in 2007 as 20% time.
- It was then first as open sourced project in 2009.
- In 2012 v1.0 was released.

## Real-life project example

I shared a project at NOTHS (the company I work for when I wrote this), it was a small search term suggester service, originally written in Ruby then gets a rewrite with Go. Point out how much faster development process in Go, performance improvements gained; such as: lower error rates, less or no zero time outs, rpm on a certain thread numbers, etc. It would help if this was presented with a side-by-side graph, so much more story you can tell with that. I did mine using [Nic Jackson's bench package](https://github.com/nicholasjackson/bench).

## Learning sources

- [Golang.org](https://golang.org)
  - the source of Go's official documentation, suggest participants take a look at [A Tour of Go](https://tour.golang.org/) at home.
- [Go standard library documentation](https://golang.org/pkg)
  - Explain that package documentation lives here (a little demo on how handy to add `pkg/bytes/#Contains` for example).
  - It is good to explore this documentation to familiar themselves to the standard library.
  - Explain the difference between `pkg` and `doc` endpoints.

## Community

- User groups & meetups
  - GoBridge
  - Women Who Go
  - LGUG
- Online Community
  - Gophers Slack Channel
  - WWGLondon Slack Channel
  - Golang Newsletter
  - Twitter
- Conferences
  - https://github.com/golang/go/wiki/Conferences

## A teaser

Assuming that by this point the installfest has been done, it's good to have a little bit play around with Go. I think the participants would very much like to see Go in action at this point, try to play with these:

- go commands
- playground

Don't go too deep or too expansive, you don't want to confuse participants too soon. Show some of the more popular one with examples and remember to say "we will learn more in the workshop..."

### go tool

https://golang.org/cmd/go/

Encourage participant to try to type this on their machine, guided for each one of the following:

- **go version**, this is a good place to start, you can show the most current version atm, highlight a couple of cool things for this version.
- **go help**, it's helpful tool :)
- **go get**, download and install packages and dependencies, **TODO**: find example of what's beneficial to get at this point of learning.

Beyond this point we need to have a working Go program to demonstrate. We can start with a simple "Hello World" program, to do that we have to explain a little bit about workspace.

Explain that:

> Go tool derives from the source code,
> it is a zero configuration tool.
> There is no need to maintain build scripts,
> but there is a catch: a prescribed directory structure is required.
> And that is what we call a workspace

### Workspace

```
  workspace/
    bin # executable binaries
    pkg # compiled object files
    src # source code
```

The first two are maintained by go tool, while the `src` is maintained by us. This would be where all of our source codes lives.

Reminder: We have set up a `$GOPATH` at the installfest this is the workspace.

As the participants to run `go env` and check where their workspace is, an example on how an existing source code structured would be handy.

### go tool (continued)

Now that we have workspace explained, it is a good time to write our "Hello world" program.

Remind participants that they have created a github account and had setup a username with it. Explain why we have to follow that structure.

Ask participants to create a file called `hello.go` under `github.com/PARTICIPANT_NAME/` with this content:


```
package main

import "fmt"

func main() {
  // This is where we say hello
  fmt.Print("Hello world")
}
```

Now we can actually play with the rest of the go tool:

- **go run**, this would compile and run the code. A little demo showing that there's a binary file generated when we run this command would be nice.

```
  $ go run hello.go
```

- **go build**, this compile packages and dependencies, demo on how it got compiled.

```
  $ ls
  $ go build
  $ ls
```

- **go clean**, show that when we run this command object files would get removed.

```
  $ ls
  $ go clean
  $ ls
```

- **go doc**, demo how documentation shown for package or symbol.

```
  $ go doc
```

### playground

- introduce playground https://play.golang.org/

## Where Go stands in the industry

I had a screenshot from http://www.itjobswatch.co.uk/jobs/uk/go.do, showing the demand in the industry has risen in the last couple of years. How many  permanent job cited. This will go well with the next section, where we introduce the many companies that has adopted Go in the current time.

## Companies using Go

You can find list of companies using Go [here](https://github.com/golang/go/wiki/GoUsers).
Why is it good to mention the many companies who has chosen the way of Go?
- established companies thinks that it's a good investment for the future.
- they believe in the technology.
- the popularity of the language.
- more job opportunities.
- this is not a toy language & I am not wasting my time (not everyone is doing this for a hobby, most participants are serious job seeker / people trying to have a career change).

At the end of name dropping would be the perfect opportunity to say:

> This is the perfect time to learn Go!
