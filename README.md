# Introduction
[Please visit The Timeline Consortium website for more detaied information.](http://timelineconsortium.org)

Our goal is to create and disseminate a **widely-agreed-upon standard for tagging rich but relatively unstructured online information** (e.g. Wikipedia, articles, manuscripts, media archives, online course co
ntent) **for use in rich timeline-style displays.**  Related  calendar standards, disciplinary standards, and language-specific standards exist. Many of these standards are richly descriptive and flexible, but they are largely not interoperable–and they are not being used in mainstream education-oriented or research- oriented timeline software today. The lack of community-driven agreement on a common standard for describing and tagging the kinds of information that timeline tools need to import and then display is presently inhibiting researchers’ and learners’ abilities to understand and compare temporal sequences in pursuits ranging from Big History to Epidemiology to Criminology to Cell Biology. 

**The Timeline Consortium** was founded in 2016 by a group of researchers and technologists from academia and industry, working together.  

*We are open to new contributors and members.  Please contact us through timelineconsortium@gmail.com. We also have a Basecamp channel where we discuss these topics, please contact us if you want to join.*

**Read more here**: 
* [Proposal to the Sloan Foundation that started this project](https://drive.google.com/open?id=1DLoRhywUbXAhzMwWha_PXFhJST7fID1BK3l3f-TkWlc).   
* [List of active consortium members](https://timelineconsortium.org/members).

**And, for reference**, here are some of the Consortium members’ **related projects:** 
* [Timeline Storyteller](http://timelinestoryteller.org) (Matthew Brehmer, Bongshin Lee, & Nathalie Henry Riche, Microsoft Research)
* [TimeLineCurator](http://timelinecurator.org) (Johanna Fulda, Cumu8; Matthew Brehmer, Microsoft Research; Tamara Munzner, University of British Columbia) 
* [Timelines Revisited: A Design Space and Considerations for Expressive Storytelling](https://timelinesrevisited.github.io/). Matthew Brehmer, Bongshin Lee, Benjamin Bach, Nathalie Henry Riche, and Tamara Munzner. In IEEE Transactions on Visualization and Computer Graphics / TVCG  (in press) 
* [Perio.do](http://perio.do) (Adam Rabinowitz, U. Texas & Ryan Shaw, UNC)
* [Dataverse](http://thedata.org) (Mercè Crosas, Gustavo Durand, Julian Gautier, Harvard) 
* [PredictionX](https://www.edx.org/course/predictionx-john-snow-cholera-epidemic-harvardx-soc1-jsx) (Alyssa Goodman, Harvard)
* [HarvardX](http://harvardx.harvard.edu/) courses on edX (Lichtenstein & Luis Duarte, Harvard)
* [Library Cloud](http://library.harvard.edu/librarycloud) (Wones, Harvard Library) 
* [Jamaican Slave Revolt Map/Timeline](http://revolt.axismaps.com/map/)  (Vincent Brown, Harvard)
* [Force11](https://www.force11.org/) (Mercè Crosas, Harvard) 
* Video Annotation Tool ([repo](https://github.com/lduarte1991/hxat)) ([description](http://annotation.chs.harvard.edu/about.php)) (Luis Duarte, Harvard)

# Timeline-Standard
Metadata standard for timelines.

We borrow from perio.do, SKOS, and schema.org/event to build a schema for timeline events. We started out with these two objects:

## TimelineEvent Object
An occurrence in a sequence, which is usually temporal. It might be a point or a range.

### ID
Identifier for the timelineEvent object (This can be an ARK, a DOI, or a local identifier).
required

### Label
A name for the event.
required

### Description
A rich-text description of the event.
optional

### Start
The beginning of the event. The value is usually a Date Time, but it could be something else. 
required

### End
The end of the event for events that are a range. When the event is a point, only "Start" is expected.
optional

## Timeline Object
A collection of TimelineEvent objects. 

### id 
Identifier for the timeline object (This can be an ARK, a DOI, or a local identifier).
required

### Label
A name for the timeline.
required

### TimelineEventList
A list or collecton of timelineEvent objects
required

# Expanding Basic Definitions
Our plan is to expand the initial basic definions to include the conclusions we came to in our April 26, 2017 Radcliffe meeting. It includes the following topics:

+ Add an uncertainty associated with various metadata values (time, labels, ...)
+ Start and End do not need to be time
+ Use of start interval and end interval, following perio.do definition
+ The standard will be specified as a JSON-LD
+ We have not decided one how to define geospatial coverage in the Timeline standard, but we want to borrow from what already exists

