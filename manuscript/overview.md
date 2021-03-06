# History and Overview of R

> There are only two kinds of languages: the ones people complain
> about and the ones nobody uses ---*Bjarne Stroustrup*

[Watch a video of this chapter](https://youtu.be/STihTnVSZnI)

## What is R? 

This is an easy question to answer. R is a dialect of S. 

## What is S? 

S is a language that was developed by John Chambers and others at the
old Bell Telephone Laboratories, originally part of AT&T Corp. S was
[initiated in 1976](http://cm.bell-labs.com/stat/doc/94.11.ps) as an
internal statistical analysis environment---originally implemented as
Fortran libraries. Early versions of the language did not even contain
functions for statistical modeling.

In 1988 the system was rewritten in C and began to resemble the system
that we have today (this was Version 3 of the language). The book
*Statistical Models in S* by Chambers and Hastie (the white book)
documents the statistical analysis functionality. Version 4 of the S
language was released in 1998 and is the version we use today. The
book *Programming with Data* by John Chambers (the green book)
documents this version of the language.

Since the early 90's the life of the S language has gone down a rather
winding path. In 1993 Bell Labs gave StatSci (later Insightful Corp.)
an exclusive license to develop and sell the S language. In 2004
Insightful purchased the S language from Lucent for $2 million. In
2006, Alcatel purchased Lucent Technologies and is now called
Alcatel-Lucent. 

Insightful sold its implementation of the S language under the product
name S-PLUS and built a number of fancy features (GUIs, mostly) on top
of it---hence the "PLUS". In 2008 Insightful was acquired by TIBCO for
$25 million. As of this writing TIBCO is the current owner of the S
language and is its exclusive developer.

The fundamentals of the S language itself has not changed dramatically
since the publication of the Green Book by John Chambers in 1998. In
1998, S won the Association for Computing Machinery’s Software System
Award, a highly prestigious award in the computer science field.

## The S Philosophy

The general S philosophy is important to understand for users of S and
R because it sets the stage for the design of the language itself,
which many programming veterans find a bit odd and confusing. In
particular, it's important to realize that the S language had its
roots in data analysis, and did not come from a traditional
programming language background. Its inventors were focused on
figuring out how to make data analysis easier, first for themselves,
and then eventually for others.

In [Stages in the Evolution of
S](http://www.stat.bell-labs.com/S/history.html ), John Chambers
writes:

> “[W]e wanted users to be able to begin in an interactive environment,
> where they did not consciously think of themselves as programming.
> Then as their needs became clearer and their sophistication increased,
> they should be able to slide gradually into programming, when the
> language and system aspects would become more important.”

The key part here was the transition from *user* to *developer*. They
wanted to build a language that could easily service both
"people". More technically, they needed to build language that would
be suitable for interactive data analysis (more command-line based) as
well as for writing longer programs (more traditional programming
language-like).


## Back to R

The R language came to use quite a bit after S had been developed. One
key limitation of the S language was that it was only available in a
commericial package, S-PLUS. In 1991, R was created by Ross Ihaka and
Robert Gentleman in the Department of Statistics at the University of
Auckland. In 1993 the first announcement of R was made to the public.
Ross's and Robert's experience developing R is documented in a 1996
paper in the *Journal of Computational and Graphical Statistics*:

> Ross Ihaka and Robert Gentleman. R: A language for data analysis and graphics. Journal of Computational and Graphical Statistics, 5(3):299--314, 1996

In 1995, Martin Mächler made an important contribution by convincing
Ross and Robert to use the [GNU General Public
License](http://www.gnu.org/licenses/gpl-2.0.html) to make R free
software. This was critical because it allowed for the source code for
the entire R system to be accessible to anyone who wanted to tinker
with it (more on free software later).

In 1996, a public mailing list was created (the R-help and R-devel
lists) and in 1997 the R Core Group was formed, containing some people
associated with S and S-PLUS. Currently, the core group controls the
source code for R and is solely able to check in changes to the main R
source tree. Finally, in 2000 R version 1.0.0 was released to the
public.



## Basic Features of R

In the early days, a key feature of R was that its syntax is very
similar to S, making it easy for S-PLUS users to switch over. While
the R's syntax is nearly identical to that of S's, R's semantics,
while superficially similar to S, are quite different. In fact, R is
technically much closer to the Scheme language than it is to the
original S language when it comes to how R works under the hood.

Today R runs on almost any standard computing platform and operating
system. Its open source nature means that anyone is free to adapt the
software to whatever platform they choose. Indeed, R has been reported
to be running on modern tablets, phones, PDAs, and game consoles.

One nice feature that R shares with many popular open source projects
is frequent releases. These days there is a major annual release,
typically in October, where major new features are incorporated and
released to the public. Throughout the year, smaller-scale bugfix
releases will be made as needed. The frequent releases and regular
release cycle indicates active development of the software and ensures
that bugs will be addressed in a timely manner. Of course, while the
core developers control the primary source tree for R, many people
around the world make contributions in the form of new feature, bug
fixes, or both.

Another key advantage that R has over many other statistical packages
(even today) is its sophisticated graphics capabilities. R's ability
to create "publication quality" graphics has existed since the very
beginning and has generally been better than competing
packages. Today, with many more visualization packages available than
before, that trend continues. R's base graphics system allows for very
fine control over essentially every aspect of a plot or graph. Other
newer graphics systems, like lattice and ggplot2 allow for complex and
sophisticated visualizations of high-dimensional data.

R has maintained the original S philosophy, which is that it provides a
language that is both useful for interactive work, but contains a
powerful programming language for developing new tools. This allows
the user, who takes existing tools and applies them to data, to slowly
but surely become a developer who is creating new tools.

Finally, one of the joys of using R has nothing to do with the
language itself, but rather with the active and vibrant user
community. In many ways, a language is successful inasmuch as it
creates a platform with which many people can create new things. R is
that platform and thousands of people around the world have come
together to make contributions to R, to develop packages, and help
each other use R for all kinds of applications. The R-help and R-devel
mailing lists have been highly active for over a decade now and there
is considerable activity on web sites like Stack Overflow. 


## Free Software

A major advantage that R has over many other statistical packages and
is that it's free in the sense of free software (it's also free in the
sense of free beer). The copyright for the primary source code for R
is held by the [R Foundation](http://www.r-project.org/foundation/)
and is published under the [GNU General Public License version
2.0](http://www.gnu.org/licenses/gpl-2.0.html).

According to the Free Software Foundation, with *free software*, you
are granted the following [four
freedoms](http://www.gnu.org/philosophy/free-sw.html)

-   The freedom to run the program, for any purpose (freedom 0).

-   The freedom to study how the program works, and adapt it to your
    needs (freedom 1). Access to the source code is a precondition for
    this.

-   The freedom to redistribute copies so you can help your neighbor
    (freedom 2).

-   The freedom to improve the program, and release your improvements to
    the public, so that the whole community benefits (freedom 3). Access
    to the source code is a precondition for this.
    
You can visit the [Free Software Foundation's web
site](http://www.fsf.org) to learn a lot more about free software. The
Free Software Foundation was founded by Richard Stallman in 1985 and
[Stallman's personal web site](https://stallman.org) is an interesting
read if you happen to have some spare time.


## Design of the R System

The primary R system is available from the [Comprehensive R Archive
Network](http://cran.r-project.org), also known as CRAN. CRAN also
hosts many add-on packages that can be used to extend the
functionality of R. 

The R system is divided into 2 conceptual parts:

1.  The "base" R system that you download from CRAN: 
[Linux](http://cran.r-project.org/bin/linux/)
[Windows](http://cran.r-project.org/bin/windows/)
[Mac](http://cran.r-project.org/bin/macosx/) [Source
Code](http://cran.r-project.org/src/base/R-3/R-3.1.3.tar.gz)

2.  Everything else.

R functionality is divided into a number of *packages*.

- The "base" R system contains, among other things, the `base` package
    which is required to run R and contains the most fundamental
    functions.

- The other packages contained in the "base" system include `utils`,
    `stats`, `datasets`, `graphics`, `grDevices`, `grid`, `methods`,
    `tools`, `parallel`, `compiler`, `splines`, `tcltk`, `stats4`.

- There are also "Recommended" packages: `boot`, `class`, `cluster`,
    `codetools`, `foreign`, `KernSmooth`, `lattice`, `mgcv`, `nlme`,
    `rpart`, `survival`, `MASS`, `spatial`, `nnet`, `Matrix`.

When you download a fresh installation of R from CRAN, you get all of
the above, which represents a substantial amount of
functionality. However, there are many other packages available:

-   There are over 4000 packages on CRAN that have been developed by
    users and programmers around the world.

-   There are also many packages associated with the [Bioconductor
    project](http://bioconductor.org).

-   People often make packages available on their personal websites;
    there is no reliable way to keep track of how many packages are
    available in this fashion.

- There are a number of packages being developed on repositories like
  GitHub and BitBucket but there is no reliable listing of all these
  packages.


## Limitations of R

No programming language or statistical analysis system is perfect. R
certainly has a number of drawbacks. For starters, R is essentially
based on almost 50 year old technology, going back to the original S
system developed at Bell Labs. There was originally little built in
support for dynamic or 3-D graphics (but things have improved greatly
since the “old days”).

Another commonly cited limitation of R is that objects must generally
be stored in physical memory. This is in part due to the scoping rules
of the language, but R generally is more of a memory hog than other
statistical packages. However, there have been a number of
advancements to deal with this, both in the R core and also in a
number of packages developed by contributors. Also, computing power
and capacity has continued to grow over time and amount of physical
memory that can be installed on even a consumer-level laptop is
substantial. While we will likely never have enough physical memory on
a computer to handle the increasingly large datasets that are being
generated, the situation has gotten quite a bit easier over time.


At a higher level one "limitation" of R is that its functionality is
based on consumer demand and (voluntary) user contributions. If no one
feels like implementing your favorite method, then it’s *your* job to
implement it (or you need to pay someone to do it). The capabilities
of the R system generally reflect the interests of the R user
community. As the community has ballooned in size over the past 10
years, the capabilities have similarly increased. When I first started
using R, there was very little in the way of functionality for the
physical sciences (physics, astronomy, etc.). However, now some of
those communities have adopted R and we are seeing more code being
written for those kinds of applications.

If you want to know my general views on the usefulness of R, you can
see them here in the following exchange on the R-help mailing list
with Douglas Bates and Brian Ripley in June 2004:

> **Roger D. Peng**: I don't think anyone actually believes that R is
> designed to make *everyone* happy. For me, R does about 99% of the
> things I need to do, but sadly, when I need to order a pizza, I still
> have to pick up the telephone.  

> **Douglas Bates**: There are several chains of pizzerias in the U.S. that provide for Internet-based ordering (e.g. www.papajohnsonline.com) so, with the Internet modules in R, it's only a matter of time before you will have a pizza-ordering function available.  

> **Brian D. Ripley**: Indeed, the GraphApp toolkit (used for the RGui interface under R for Windows, but Guido forgot to include it) provides one (for use in Sydney, Australia, we presume as that is where the GraphApp author hails from).  Alternatively, a Padovian has no need of ordering pizzas with both home and neighbourhood restaurants ....

At this point in time, I think it would be fairly straightforward to
build a pizza ordering R package using something like the `RCurl` or
`httr` packages. Any takers?


## R Resources

### Official Manuals 

As far as getting started with R by reading stuff, there is of course
this book. Also, available from [CRAN](http://cran.r-project.org) are

-   [An Introduction to R](http://cran.r-project.org/doc/manuals/r-release/R-intro.html)

-   [R Data Import/Export](http://cran.r-project.org/doc/manuals/r-release/R-data.html)

- [Writing R
    Extensions](http://cran.r-project.org/doc/manuals/r-release/R-exts.html):
    Discusses how to write and organize R packages

- [R Installation and
    Administration](http://cran.r-project.org/doc/manuals/r-release/R-admin.html):
    This is mostly for building R from the source code)

- [R
    Internals](http://cran.r-project.org/doc/manuals/r-release/R-ints.html):
    This manual describes the low level structure of R and is
    primarily for developers and R core members

- [R Language
  Definition](http://cran.r-project.org/doc/manuals/r-release/R-lang.html):
  This documents the R language and, again, is primarily for
  developers

### Useful Standard Texts on S and R

- Chambers (2008). *Software for Data Analysis*, Springer

- Chambers (1998). *Programming with Data*, Springer: This book is
    *not* about R, but it describes the organization and philosophy of
    the current version of the S language, and is a useful reference.

- Venables & Ripley (2002). *Modern Applied Statistics with S*,
    Springer: This is a standard textbook in statistics and describes
    how to use many statistical methods in R. This book has an
    associated R package (the `MASS` package) that comes with every
    installation of R.

- Venables & Ripley (2000). *S Programming*, Springer: This book is a
    little old but is still relevant and accurate. Despite its title,
    this book is useful for R also.

- Murrell (2005). *R Graphics*, Chapman & Hall/CRC Press: Paul Murrell
    wrote and designed much of the graphics system in R and this book
    essentially documents the underlying details. This is not so much
    a "user-level" book as a developer-level book. But it is an
    important book for anyone interested in designing new types of
    graphics or visualizations.

- Wickham (2014). *Advanced R*, Chapman & Hall/CRC Press: This book by
  Hadley Wickham covers a number of areas including object-oriented
  programming, functional programming, profiling and other advanced
  topics.

### Other Resources

- Major technical publishers like Springer, Chapman & Hall/CRC have
    entire series of books dedicated to using R in various
    applications. For example, Springer has a series of books called
    *Use R!*.

- A longer list of books can be found on the [CRAN web
    site](http://www.r-project.org/doc/bib/R-books.html).
