# Why Go? - DRAFT WORK IN PROGRESS

Imagine that you're on your first step into coding, this would be the first question to pop in your head, why should I learn Go? why not any other language? Ruby? C++? Java?

The answer is simple, because Go is awesome! but why? Well.. this is what you'll learn through the workshop. (I found this answer quite catchy)

At this point, I'd share a personal story, something like:
- what my background is.
- how I got into coding.
- how my journey with Go started.

Now that people warmed up to the idea, we can actually start introducing what's in the store.

## Oh the fancy words!

- Fast
- Fun
- Productive

**TODO:**

- justify the three aspects above
- include brad fitzpatrick slide from Japan GoConf'15
- introduce concurrency in a simple analogy

## Real-life project example

I shared a project at NOTHS (the company I work for when I wrote this), it was a small search term suggester service, originally written in Ruby then gets a rewrite with Go. Point out how much faster development process in Go, performance improvements gained; such as: lower error rates, less or no zero time outs, rpm on a certain thread numbers, etc. It would help if this was presented with a side-by-side graph, so much more story you can tell with that. I did mine using [Nic Jackson's bench package](https://github.com/nicholasjackson/bench).

## Learning sources

- [Golang.org](https://golang.org)
  - the source of Go's official documentation, take a look at [A Tour of Go](https://tour.golang.org/)
- [Go official package documentation](https://golang.org/pkg)
  - Explain that package documentation lives here (a little demo on how handy to use `pkg/bytes/#Contains` for example)
  - Explain the difference between `pkg` and `doc`

## Community

- GoBridge
- Women Who Go
- Newsletter
- Twitter
- Conferences
- slack

## A teaser

Assuming that by this point the installfest has been done, it's good to have a little bit play around with Go. I think the students would very much like to see Go in action at this point, try to play with these:

- go commands
- playground

Don't go too deep or too expansive, you don't want to confuse participants too soon. Show some of the more popular one with examples and remember to say "we will learn more in the workshop..."

### go commands

https://golang.org/cmd/go/

- **go version**, this is a good place to start, you can show the most current version atm, highlights a couple of cool things for this version.
- **go doc**, demo how documentation shown for package or symbol.
- **go get**, download and install packages and dependencies, **TODO**: find example of what's beneficial to get at this point of learning.
- **go build**, this compile packages and dependencies, demo on how it got compiled.
- **go clean**, show that when we run this command object files would get removed.
- **go run**, a little demo showing that there's a binary file generated when we run this command would be nice.

### playground

- a little history
- explain the machine on playground
- explain why time now in playground points to ...
- Hello world! (maybe *Ellie McHugh*'s version)
  - Compilers and Go compilers
  - Intro into coding, introduce Variable, Constant, If condition

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
