Olympia Software Craftsmanship Workshop
=======================================
Saturday, June 6th, 2009, 10am-4pm
[Olympia Center][1]

# Overview

The Olympia Software Craftsmanship Workshop is one day workshop,
developed with the intention of increasing the level of awareness of
practices and skills that can improve our software.

Any developer interested in improving and learning new skills is
welcome.

We're going to focus on a scenario for a feature a customer
wants. We'll do it first using classic ASP.NET techniques. We'll show
how it's difficult to maintain, extend, and test.

Next, we'll use the techniques to componentize business functionality,
extracting it from the code behind in the ASP.NET project.

We'll then add a new feature to the application, using our tests to
make sure nothing has been broken in the process.

We'll finish off by going over some other tools and techniques that
can augment what we've discussed.

# User Stories

To support this workshop, (and other activities and events), we’ve
decide to create a fictional customer, in a (mostly) fictional
world. The fictional customer company will have employees, clients, a
website, products, services, an attitude, etc. As we flesh it out, it
can provide endless possibilities in terms of realistic examples.

While we do need realistic examples in terms of specific functional
requirements, we do not want to be bored either, so humor is allowed
and encouraged. (No real names should or will be used, to keep any
real person or organization taking offense).

Let's use this theme any way that's useful. Consider it
open-source. By building out more of the fictional world around the
theme, we can apply it to all kinds of exercises. With a little
planning, we can logically connect the exercises whether by parallels
or by contrasts.

# Principles

The principles we want to focus on are:

* Using User Stories and TDD to focus on real customer value
* Refactoring legacy code to make it testable *before* adding new features
* [S.O.L.I.D.][2]
* [INVEST][3]
* [Individuals and interactions over processes and tools][4]

# First Cut

We're going to do a first cut just building a plain old ASP.NET web
forms application. We'll think about the first scenario in the
stories, not considering the second story.

We'll create a web form with a [master detail view][5] add a data
source control, wire it with SQL in properties and all.

Next we'll look at adding the second scenario and show how it's
difficult with the poor design we've slapped together.

We'll consider things like extracting the SQL into a stored procedure
and other steps we might take to get this under control, and discuss
the pros and cons of each approach.

# Refactoring

We'll use the safe refactorings outlined in [Michael Feathers][6] book
to build seams and make the code we have so far testable.

First, we'll pull the data access code out of the ASPX page and into a
service.  We'll have the code behind be responsible for creating the
service and satisfying any dependencies it has.

Next we'll discuss what's wrong with having the code behind be
responsible for creating the service and we'll look at some things we
could do the address those issues.

Once we have tests around the existing application - at least the part
we are working on - we can move onto the next feature.

# TDD

We'll build another feature from scratch using TDD. We'll write the
tests for the code we wished we had then implement the feature.

# Other Practices

To wrap up, we'll touch on some other practices that make everything
work better:

* One-Step Builds
* Continuous Integration
  - TeamCity
  - Hudson
* Agile Estimation

[1]: http://maps.google.com/maps?f=q&source=s_q&hl=en&geocode=&q=olympia+center,+olympia,+wa&sll=37.0625,-95.677068&sspn=49.57764,114.257812&ie=UTF8&ll=47.041469,-122.913322&spn=0.083993,0.22316&t=h&z=13&iwloc=E
    "Olympia Center, on Google Maps"
[2]: http://blog.objectmentor.com/articles/2009/02/12/getting-a-solid-start
    "Getting a SOLID Start"
[3]: http://xp123.com/xplor/xp0308/index.shtml
    "INVEST in Good Stories, and SMART Tasks"
[4]: http://agilemanifesto.org/
    "Manifesto for Agile Software Development"
[5]: http://designingwebinterfaces.com/designing-web-interfaces-12-screen-patterns
    "12 Standard Screen Patterns"
[6]: http://www.amazon.com/gp/product/0131177052/ref=s9_sims_c2_s1_p14_i2?pf_rd_m=ATVPDKIKX0DER&pf_rd_s=center-2&pf_rd_r=0S8D0VHK1WGVWC6Q21Q7&pf_rd_t=101&pf_rd_p=470938631&pf_rd_i=507846
    "Working Effectively with Legacy Code"



