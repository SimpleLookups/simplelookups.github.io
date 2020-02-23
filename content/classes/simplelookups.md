---
author: "Russell Patterson"
date: 2013-12-21 23:32:07+00:00
draft: false
title: SimpleLookups Class
type: page
url: /classes/simplelookups/
---

This is the main static class of the SimpleLookups package.

##### Namespace Import

    using SimpleLookups;

### Jump To
* [Initialize (string)](#initialize-string)  
* [Initialize (string, bool, int)](#initialize-string-bool-int)  
* [Initialize (string, string, string, string, string, string, bool)](#initialize-string-string-string-string-string-string-bool)  
* [Initialize (string, string, string, string, string, string, bool, bool, int)](#initialize-string-string-string-string-string-string-bool-bool-int)  
* [AddConnectionString](#addconnectionstring)  

---
### Initialize (string)
Initializes SimpleLookups with the default connection string.
##### Signature
    static void Initialize(
        string defaultConnectionString
    );
##### Available
1.0+

---
### Initialize (string, bool, int)
Initializes SimpleLookups with the default connection string, and the provided cache settings.
##### Signature
    static void Initialize(
        string defaultConnectionString, 
        bool enableCaching, 
        int cacheRefreshPeriod
    );
##### Available
2.0+

---
### Initialize (string, string, string, string, string, string, bool)
Initializes SimpleLookups with the default connection string, and the provided column prefixes.
##### Signature
    static void Initialize(
        string defaultConnectionString, 
        string idColumnPrefix, 
        string nameColumnPrefix, 
        string descriptionColumnPrefix, 
        string codeColumnPrefix, 
        string activeColumnName, 
        bool prefixColumnNamesWithTableName
    );
##### Available
1.6+

---
### Initialize (string, string, string, string, string, string, bool, bool, int)
Initializes SimpleLookups with the default connection string, the provided column prefixes, and the provided cache settings.
##### Signature
    static void Initialize(
        string defaultConnectionString, 
        string idColumnPrefix, 
        string nameColumnPrefix, 
        string descriptionColumnPrefix, 
        string codeColumnPrefix, 
        string activeColumnName, 
        bool prefixColumnNamesWithTableName, 
        bool enableCaching, 
        int cacheRefreshPeriod
    );
##### Available
2.0+

---
### AddConnectionString
Adds another connection string that can be used by the CRUD operations. You can reference the connection string by the connectionName you've provided here, in the operations on LookupManager.
##### Signature
    static void AddConnectionString(
        string connectionName, 
        string connectionString
    );
##### Available
1.0+

