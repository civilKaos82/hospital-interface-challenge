# Hospital Interface 
 
## Summary 
We're going to build an interface for interacting with hospital data—simplified, fake hospital data ... no [HIPAA violations][wikipedia hipaa privacy].  This is a fairly open-ended challenge.  The expectations are fairly loose, so we'll be making most of the decisions about how to design and build our program.  We'll talk things out as a pair, go to the whiteboard, maybe argue about naming, and of course, have fun!  The world is our oyster, as it were.

The goal of this challenge is to explore the utility of object-oriented design.  We'll should end up building multiple classes.  Our classes should be well-defined with a single responsibility.  The classes should have clean, flexible interfaces that allow for objects to effectively send messages to each other.  And, as always, we should use effective naming conventions.


### Create Objects as We Go
In the real-world, the data for our application would almost inevitably reside in a database.  We'll get to working with databases soon, but for this challenge, we'll just have to make up data as we go.  As an example, if we were building an animal shelter application and needed to list the pets at a shelter, we'd have to make objects to represent the shelter and the pets (see Figure 1).  We'll be doing to same thing for our hospital application:  creating objects representing fake patients, fake patient records, fake doctors, etc.

```ruby
shelter_animals = [
  Dog.new({ :name => "Jayda" }),
  Cat.new({ :name => "Bailey" }),
  Dog.new({ :name => "Tenley" }),
  Bird.new({ :name => "Tito" })
]

shelter = AnimalShelter.new({ :name => "Not a Pound", :animals => shelter_animals })
```
*Figure 1*.  Creating an animal shelter with animals—an example for creating objects to use later.


## Releases
### Release 0: Display All Admission Records
```
Admit Time         Discharge Time     Patient Name      Attending Physician
===========================================================================
2016-01-01 16:45   2016-01-02 12:30   Mavuto Beutel     Yaffe Kappel
2016-01-01 19:10   2016-01-05 11:45   Ufuoma Lane       Yin Hou
2016-01-02 01:05   2016-01-02 20:00   Aaren MacAngus    Ellar Pearce
2016-01-02 14:45   2016-01-06 12:15   Brad Patterson    Ellar Pearce
2016-01-03 16:30   2016-01-04 12:20   Agata Polzin      Yin Hou
2016-01-03 16:35                      Aaren MacAngus    Yaffe Kappel
2016-01-04 10:45                      Mavuto Beutel     Yaffe Kappel
```
*Figure 2*.  Example admission record output, showing all records.

We'll start building our application with a feature that displays patient admission records.  When our application runs, all admission records are displayed.  The output should resemble Figure 2, but it does not need to be an exact copy.

As was written in the *Summary*, we'll decide how to design and build our program.  The only requirement is that we're testing the behavior of any objects that we create.  







###Release 1 : Build Authentication System

Now imagine you're delivering this software and it's going to run as a Ruby file in Terminal. 

You're going to create a single administrator who can add employees and patients, and only this administrator is allowed to create these objects in the system.

You also want to allow the created employees and patients to login and access their medical records. However, a janitor logging in will not be able to access sensitive patient data.

An example of how this interface might look (this is just an idea - you are welcome to implement this feature however you think is best):

```text
$ ruby hospital.rb
> Welcome to Misty River Hospital
> -------------------------------
> Please enter your username:
> ruby_tuesday
> Please enter your password:
> ********
> -------------------------------
> Welcome, ruby_tuesday.  Your access level is: DOCTOR
> -------------------------------
> What would you like to do?
> Options:
> - list_patients
> - view_records <patient_id>
> - add_record <patient_id>
> - remove_record <patient_id> <record_id>
``` 


##Optimize Your Learning 

As you are coding, ask yourself...

 * How will I use this class?
 * How will this class interact with the other classes?
 * Does this attribute need to be private or public?
 * Are my methods and variables well named?


##Resources


[wikipedia hipaa privacy]: https://en.wikipedia.org/wiki/Health_Insurance_Portability_and_Accountability_Act#Privacy_Rule



