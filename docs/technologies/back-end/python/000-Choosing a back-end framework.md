# Choosing a Rest API framework/library

## Status

Proposed

## Context

Choosing a backend framework is a non-trivial and non-unique decision in the context of micro-services.
For each programming language there's at least one implementation of a webserver/http-library/framework to choose from.
The criteria for judging the options are many and often in contrast between each other.

Whereas simplicity might be an important need, lack of mature features might undermine the final result in more complex projects.
In the case, instead, of choosing an entire framework the risk of remaining tightly bounded to specific technologies might represent a problem 
in an ever-changing panorama like  the software development one.

### Goal

The goal of this article is to provide the reader with a summary of frameworks that he can choose from with pro and cons and use-cases that are a better
fit for one or another of the analyzed tools.

In general we'll focus on tools for the creation of Rest APIs. 
With the advent of Single Page Applications and Mobile Apps i consider 
* rendering HTML pages
* serving static files
* redirecting to error pages
* implementing forms
no more a responsibility of the Application Web Server.

Some of the tools highlighted in this comparison will allow you to implement the previous requirements as well but these features won't be taken into consideration
when trying to understand pro and cons.


### Programming Language
The first variable in the equation is for sure the choice of a programming language.

In this article i'll try to focus on 2 main programming languages:
* Python
* TypeScript on NodeJS

While several other languages might offer better performances (Go, Rust, C++) or a most established support-base for the development of WebServers (Java, C#), 
Python and JavaScript (TypeScript) are, at the moment, [the most popular languages](https://githut.info/) in the open source world.

The popularity of these languages might affect in a positive way:
* ease of hiring new developers
* development libraries available
* support from the community

The drawback of these two languages, in the development of Application Web Servers, is the relative immaturity when compared to Java and or C# and the lower performances when 
compared to other multi-core-optimized languages such as Rust or Go.

I believe though that the possibilities offered from these 2 languages place them in a sweet spot which gives a good compromise between performace and ease of use.

### Framework vs Library



### Performance vs Extensibility







https://www.djangoproject.com/

https://www.django-rest-framework.org/

## Decision

When creating a core service, with complex domain rules, evaluate django with the django rest framework

## Consequences

Evaluate: https://github.com/clarkduvall/serpy