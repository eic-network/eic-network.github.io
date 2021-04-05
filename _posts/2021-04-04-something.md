---
title: something
---

Collections
Collections are a great way to group related content like members of a team or talks at a conference.

SetupPermalink
To use a Collection you first need to define it in your _config.yml. For example here’s a collection of staff members:

collections:
  - staff_members
In this case collections is defined as a sequence (i.e., array) with no additional metadata defined for each collection. You can optionally specify metadata for your collection by defining collections as a mapping (i.e., hashmap) instead of sequence, and then defining additional fields in it:

collections:
  staff_members:
    people: true
