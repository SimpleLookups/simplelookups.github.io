---
author: "Russell Patterson"
date: 2013-12-21 23:34:16+00:00
draft: false
title: LookupManager Class
type: page
url: /classes/lookupmanager/
---

Manages a single lookup type.

##### Namespace Import

    using SimpleLookups;

### Jump To
* [Constructor](#constructor)  
* [Create](#create)  
* [Get (int)](#get-int)  
* [Get (IList&lt;int&gt;)](#get-ilistltintgt)  
* [Get (string)](#get-string)  
* [Get (IList&lt;string&gt;)](#get-ilistltstringgt)  
* [Get (bool)](#get-bool)  
* [Update](#update)  
* [Delete (int)](#delete-int)  
* [Delete (IList&lt;int&gt;)](#delete-ilistltintgt)  
* [Delete (string)](#delete-string)  
* [Delete (IList&lt;string&gt;)](#delete-ilistltstringgt)  
* [Deprecated and Removed Methods](#deprecated-and-removed-methods)
    * [GetById](#getbyid)  
    * [GetAll](#getall)  
    * [GetActive](#getactive)  

---
### Constructor
Creates a new instance of LookupManager to manage lookups of type ```T```. ```T``` must implement [```SimpleLookups.Interfaces.ILookup```](/interfaces/ilookup/) somewhere in it's inheritance chain, or inherit from [```SimpleLookups.Lookup```](/classes/lookup/).
##### Signature
    LookupManager<T>();
##### Available
1.0+

---
### Create
Creates an entry in the lookup table of that specific type. If the record is not created, but there is no error, the method returns false. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    bool Create(T lookup);
    bool Create(T lookup, string connectionName); 
##### Available
1.0+

---
### Get (int)
Retrieves the matching entry for the provided id. If no record is found, returns null. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    T Get(int id); 
    T Get(int id, string connectionName); 
##### Available
1.1+

---
### Get (IList&lt;int&gt;)
Retrieves the matching entries for the provided ids. If no records are found, returns an empty list. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    T Get(IList<int> ids);
    T Get(IList<int> ids, string connectionName); 
##### Available
1.1+

---
### Get (string)
Retrieves the matching entry for the provided code. If no record is found, returns null. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    T Get(string code);
    T Get(string code, string connectionName);
##### Available
1.2+

---
### Get (IList&lt;string&gt;)
Retrieves the matching entries for the provided codes. If no records are found, returns an empty list. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    T Get(IList<string> codes); 
    T Get(IList<string> codes, string connectionName); 
##### Available
1.2+

---
### Get (bool)
Retrieves all of the lookups of the type if the activeOnly flag is false. Returns only active lookups if the activeOnly flag is true. If no records are found, returns an empty list. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    IList<T> Get(bool activeOnly);
    IList<T> Get(bool activeOnly, string connectionName);
##### Available
1.2+

---
### Update
Updates an existing record by id. If the record isn't found, the method will return false. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    bool Update(T lookup); 
    bool Update(T lookup, string connectionName); 
##### Available
1.0+

---
### Delete (int)
Removes an existing record by its id. If the record isn't found, the method will return false. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    bool Delete(int id); 
    bool Delete(int id, string connectionName); 
##### Available
1.0+

---
### Delete (IList&lt;int&gt;)
Removes existing records by ids. If all of the records aren't found, the method will return false. If any are deleted, it will return true. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    bool Delete(IList<int> ids); 
    bool Delete(IList<int> ids, string connectionName);  
##### Available
1.1+

---
### Delete (string)
Removes an existing record by its code. If the record isn't found, the method will return false. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    bool Delete(string code); 
    bool Delete(string code, string connectionName); 
##### Available
1.2+ 

---
### Delete (IList&lt;string&gt;)
Removes existing records by codes. If all of the records aren't found, the method will return false. If any are deleted, it will return true. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    bool Delete(IList<string> codes); 
    bool Delete(IList<string> codes, string connectionName); 
##### Available
1.2+

---
## Deprecated and Removed Methods

---
### GetById
Retrieves the matching entry for the provided id. If no record is found, returns null. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    T GetById(int id);  
    T GetById(int id, string connectionName); 
##### Available
1.0; **Removed 1.1**
##### Migration Strategy
Uses of this method should be migrated to Get(int).

---
### GetAll
Retrieves all of the lookups of the type. If no records are found, returns an empty list. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
##### Signature
    IList<T> GetAll();
    IList<T> GetAll(string connectionName);
##### Available
1.0-1.1; **Deprecated 1.2; Removed 1.5**
##### Migration Strategy
Uses of this method should be migrated to Get(bool), passing in false.

---
### GetActive
Retrieves all of the lookups of the type having their Active flag set to 1. If no records are found, returns an empty list. If an error occurs, this method will throw a SimpleLookupsException. Check InnerException for details on the error.
###### Signature
    IList<T> GetActive();
    IList<T> GetActive(string connectionName);
###### Available
1.0-1.1; **Deprecated 1.2; Removed 1.5**
###### Migration Strategy
Uses of this method should be migrated to Get(bool), passing in true.