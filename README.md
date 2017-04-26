# Introduction

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

