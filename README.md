# intercity

> A web framework for people wanting to build microservices good 
> and build other stuff good too.

Intercity is a reasonable web framework. Others are faster, but this 
is might be more economical. Intercity provides a comfortable ride
with low cognitive cost.

Async code is difficult. And largely unnecessary. The C10k problem isn't
a problem in today's world. We have cloud servers these days. It's okay
to scale out horizontally when needed. We're not stuck to a single box.

When you're coding with intercity, you can do what you want. Each request
is served by its own thread. if you want to connect to a database, then 
connect to a database. If you want to write to a file, then write to 
a file.

## Status

Just an idea. Nothing works.

## Idea

Create an opinonated stack that uses synchronous (blocking) I/O. There are
very few frameworks that have avoided async. Perhaps only `rouille`.

My problem with `rouille` is that it makes you do too much thinking. I 
don't want to decide on a templating language every time.

Stack

- http: tiny-http, rustls
- routing: intercity
- everything in the middle: intercity
- model: diesel
- views: minijinja, HTMX

## Why "intercity"?

It's a refererce to cheap, high-quality train services in Europe, combined
with the Ruby on Rails and Express web framework names.
