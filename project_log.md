SET11516 
========
Advanced Software Engineering Team Working
------------------------------------------
40056761 - Project Log
--------------------

The goal of this document is to record and catalogue the progress made by Sam
Dixon (40056761) during the progress of the SET11516 team working project.


2017-09-04
----------
Start of term. Rasmus said that he had to keep a log of work he did during the
teamwork project, so I have opted to write mine using markdown, for ease and
speed. 


2017-09-07
----------
First team working lecture.
Was surprised by the number of people, as Gareth was the only other masters
student I was aware of - There is potential for multiple teams to form.

There is a good mix of interests and skills among the class, so teams should
be well rounded in terms of disciplines.

Sally has asked us to come up with some ideas/interests that we can brainstorm
in the coming weeks.

Gareth has created a Slack group for us to use to communicate.


2017-09-10
----------
There are now 5 of us on the Slack group, and of them I have worked with 3
previously.

There were 9 of us in the lecture, so we will need to try and get them on
Slack ASAP so we can start sharing ideas.


2017-09-14
----------
Second lecture.
People were sharing more of their interests, as well as technologies/
applications currently in the spotlight.

We pushed the Slack group during the lecture, and everyone said they would get
on it.

I said that I would create a Trello board as a means of organising
resources, etc.  

I have set up a Trello page, but getting to interface with Slack properly is
proving more awkward than I feel it should.


2017-09-18
----------
There are now 8 of us on Slack (not including Sally).

Not much conversation happening yet, but people are still settling in the
term.


2017-09-21
----------
Third Lecture.

There seems to be two distinct interests between students: Mobile
applications or Genetic/Evolutionary computing.

Sally is pushing for us each to come with a semi-concrete idea to the next
lecture.

Some good idea discussion on Slack, and Sally has mentioned Emma Hart has been
asking for more robot based projects - which might be quite fun.


2017-09-25
----------
We decided to split into distinct groups today on Slack.  We used a poll to
show our interest between a GA project or a mobile app project. 

Angelos, Gareth, and myself have opted to be part of the Genetic Algorithm
group, hopefully this will encourage us to focus on distinct ideas.


2017-09-26
----------
Talked to Kevin Chalmers about project ideas.
He said a previous masters student (Rob) was working with the robots and an
Nvidia Tesla.

Seemed like an interesting idea of speeding the robots behavioural logic.


2017-09-28
----------
We chose groups today, we were each asked to put our name next to a project we
found interesting.

The choices that we settled on were the Robots and an AR tourism app.

Gareth, Angelos and Myself have all opted to be in the Robot team.
There is a lot of potential avenues/techniques that can be done with the
robots - parallel processing, GA, hardware, etc.

Will have to come up with a finalised project idea soon.


2017-10-12
----------
Finalised project idea.
We want to use the Tesla and the robots in tandem to simulate and execute an
operation or "mission" simultaneously.

What the mission is, or the kind of parallel processing that will be performed
does need to decided, but that can be determined during the development
stage.


2017-10-14
----------
School of Computing Open Day.
Helped Andreas set up the robots, and explained how they worked to potentail
students.

Got a good opportunity to talk Andreas about the project and get some tips,
insight on how to progress.


2017-10-16
----------
Talked to Emma Hart about potential robot projects.
She mentioned a technique called "MapElite" that based around the concept of
simulating multiple criteria combinations and then selecting the most
appropriate for the situation.
This idea could work quite well considering the parallel nature of the Tesla
card.


2017-10-19
----------
Been reading some of the papers I have found.
Adding to lit review (sparse).

2017-10-23
----------
Working on the project pitch with Gareth.
Using Google Docs for convenience.
Outlined the topics we want to cover during the presentation.
Will continue adding content to slides in  between coursework.

2017-10-25
----------
Talked to Andreas again, he mentioned some papers I should try to find and
look at.
I have taken note of them to use in a literature review.


2017-11-02
----------
Project Pitch
I feel the pitch went well, we were within our time constraints and could
provide answers to all the asked questions.


2017-11-08
----------
Tech Meet Up
Everyone is required to introduce themselves at the start of the event.
When I mentioned the robot project a member of staff from Robert Gordon
mentioned that we should check out the Edinburgh Robotic Forum.
Will have to research this later.


2017-11-21
----------
Been searching for further papers.

Found a few relevant ones in regards to using cheaper hardware (!) and using
SLAM on small indoor robots.


2017-12-17
----------
Exam period starts.
Teamwork will be on the back-burner as I am focusing on Exams.

Will try to do some over the Christmas break (unlikely)


2017-12-06
----------
Further research and documentation.
There is no shortage of papers that use SLAM.

Found a few more that describe primitive mapping using very limited sensors.



2018-01-08
----------
Trimeter 2 begins.

As expected, very little work occurred over Christmas.

Gareth has got the Simulator building and running on Debian.

I have got a loose literature review of relevant papers.


2018-01-14
----------
First meeting back with Sally.

We had the simulator and the as well as the PS4 controller working, so we were
able to demonstrate a working Linux build with the physical robot and the
simulator.

Gareth has passed the build info onto me and given me a quick rundown of how
to build/execute the simulator.


2018-01-15
----------
Have gone through the processes of building the simulator.
The process is complicated due to the required systems being spread over 3
repositories.

The python shell can interface directly with the simulator or the physical
robot.

Current goal is to implement some form of SLAM as per the papers I have
gathered.


2018-01-19
----------
Had a quick chat with Jon Kerridge.
He was saying how two of his honours students are working on projects with the
Thymio II bots, and had hit some snags. 
Jon's students are trying to use a Java wrapper to send commands to the robots
via D-bus.
I told Jon about our progress, and that we ar enow able to use python to send
commands via D-bus.
He has asked if myself and Gareth would be in next Wednesday to chat to his
students.


2018-01-22
----------
Worked on a rough draft of our report today.
Introduction boilerplate and a brief introduction to each section.


2018-01-25
----------
Found an extremely detailed and useful paper title 'SLAM for Dummies'.
While the name is somewhat tongue-in-cheek, the paper details clearly how to
implement SLAM using the Extended Kalman Filter (EKF).


2018-01-26
----------
There exists an issue with the Thymio II robot's odometry (or lack here of).
The robots us naive motors that do not track distance travelled, but they can
utilise simple Dead-Reckoning.

[I have found a software library for the Thymio II][1] that claims to
implement some form of odometry via software.


2018-01-28
----------
There exists several paper detailing attempts to deal with the Thymio II's
lack of odometry, but most are highly experimental.

It seems we have to design some form of calibration or use "magic-numbers" to
make dead reckoning usable.


2018-01-30
----------
The two requirements for implementing SLAM are some form of odometry and
sensors.
The current goal is to implement some form of Dead reckoning - where you
estimate the current position of the robot based off of the speed of the
motors and the time they were moving.

While dead reckoning is not as accurate as odometry, but will still allow for
SLAM to operate.

The robots in the simulator have a maximum speed of 500 'units' - according to
Andreas this relates quite accurately to the real robots.

The previous [link][1] contains a git repo that lists a speed coefficient of
2.93 and wheel radius of 95mm (this is the only measurement that seems
grounded in reality).
`
Using the found metrics, it should be possible to implement a system that will
allow for approximation of a location in 2D space.

Current steps consist of confirming that the 'magic-numbers' pulled from the
repo match up with our version.


2018-02-06
----------
Conducted some preliminary tests with our system to check the authenticity of
the 'magic-numbers'.

It seems that each of the wheel motors can be issued a target speed, and the
current speed of each motor can be queried - with them capping out at 500.

Tests need to be conducted to check the speed coefficient is valid, then a
delta time can be calculated for the distance travelled in a set amount of
time.

[1]:http://wiki.ros.org/thymio_navigation_driver
