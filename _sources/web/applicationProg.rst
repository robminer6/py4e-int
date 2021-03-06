Application Programming Interfaces
----------------------------------
.. index::
    single: API
    single: SOA
    single: Web Services
    single: Service-Oriented Architecture

We now have the ability to exchange data between applications using
HyperText Transport Protocol (HTTP) and a way to represent complex data
that we are sending back and forth between these applications using
eXtensible Markup Language (XML) or JavaScript Object Notation (JSON).

The next step is to begin to define and document "contracts" between
applications using these techniques. The general name for these
application-to-application contracts is *Application Program
Interfaces* (APIs). When we use an API, generally one program
makes a set of *services* available for use by other
applications and publishes the APIs (i.e., the "rules") that must be
followed to access the services provided by the program.

.. fillintheblank:: webAPI_fill1
    :practice: T

    APIs are ________ between applications that exchange data using HTTP and representing complex data using XML or JSON.

    - :[Cc]ontract(s)*: An API is the general name for an application to application contract.
      :.*: An API is an agreement between the two applications, also known as....

When we begin to build our programs where the functionality of our
program includes access to services provided by other programs, we call
the approach a *Service-oriented architecture* (SOA). A
SOA approach is one where our overall application makes use of the
services of other applications. A non-SOA approach is where the
application is a single standalone application which contains all of the
code necessary to implement the application.

.. mchoice:: webAPI_MC_tf
    :practice: T
    :answer_a: False
    :answer_b: True
    :correct: b
    :feedback_a: Try again!
    :feedback_b: By including access to services provided by other programs in the functionality of a program, you are using an SOA approach. 

    True or False? A service-oriented architecture makes use of other applications' services.

We see many examples of SOA when we use the web. We can go to a single
web site and book air travel, hotels, and automobiles all from a single
site. The data for hotels is not stored on the airline computers.
Instead, the airline computers contact the services on the hotel
computers and retrieve the hotel data and present it to the user. When
the user agrees to make a hotel reservation using the airline site, the
airline site uses another web service on the hotel systems to actually
make the reservation. And when it comes time to charge your credit card
for the whole transaction, still other computers become involved in the
process.

.. figure:: ../images/soa.svg
   :alt: Service-oriented architecture

A Service-oriented architecture has many advantages, including: (1) we
always maintain only one copy of data (this is particularly important
for things like hotel reservations where we do not want to over-commit)
and (2) the owners of the data can set the rules about the use of their
data. With these advantages, an SOA system must be carefully designed to
have good performance and meet the user's needs.

When an application makes a set of services in its API available over
the web, we call these *web services*.

.. mchoice:: webAPI_MC_soa
    :practice: T
    :answer_a: It maintains only one copy of data.
    :answer_b: It is designed to meet the user's needs.
    :answer_c: It is automatically implemented.
    :answer_d: It allows the owners of the data to set the rules about the use of their data.
    :correct: c
    :feedback_a: SOA maintains only one copy of the user's data.
    :feedback_b: SOA is designed to meet the user's needs.
    :feedback_c: SOA is not automatically implemented, it is an approach taken to when building a program.
    :feedback_d: SOA allows the owners of data to set rules about the use of their data.

    Which of the following is **not** an advantage of a service oriented architecture?
