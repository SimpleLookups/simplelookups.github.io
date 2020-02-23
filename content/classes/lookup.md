---
author: "Russell Patterson"
date: 2020-02-23 13:47:29+00:00
draft: false
title: Lookup Class
type: page
url: /classes/lookup/
---

Abstract class with a base implementation of [```ILookup```](/interfaces/ilookup/).
##### Namespace Import

    using SimpleLookups;

### On This Page
[Id](#id)  
[Name](#name)  
[Description](#description)  
[Code](#code)  
[Active](#active)

---
### Id
A unique id associated with the lookup value. This is how the value should be referenced in other tables.
##### Signature
    int Id { get; set; }
##### Available
1.0+

---
### Name
The name of the lookup value.
##### Signature
    string Name { get; set; }
##### Available
1.0+

---
### Description
A brief description of the lookup value.
##### Signature
    string Description { get; set; }
##### Available
1.0+

---
### Code
A unique, user-readable string that represents this lookup.
##### Signature
    string Code { get; set; }
##### Available
1.0+

---
### Active
A boolean value indicating whether the lookup is marked active.
##### Signature
    bool Active { get; set; }
##### Available
1.0+
