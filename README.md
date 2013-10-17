Property loader [![Build Status](https://travis-ci.org/TNG/property-loader.png?branch=master)](https://travis-ci.org/TNG/property-loader)
===============

#### Table of Contents
[What It Is](#what-is-it)    
[Quick Start](#quick-start)  
[Advanced Configuration](#advanced-configuration)  
[Processing Features](#processing-features)  
[Usage example](#usage-example)  
[Java Doc](#java-doc)  

What It Is
----------

The property loader is a java library for managing property configurations.

It supports several property loading strategies and features e.g.:

1. Hierarchical/Ordered Property Loading (Master, User, System properties ....)
2. Property templates
3. Recursive Property Resolution
4. Property encryption

Quick Start
-----------

1. Build the lib
```
$ maven install
```
2. Include jar file to your application
3. Add property files eg props.properties to your applications classpath
4. Load properties

```java
        PropertyLoader propertyLoader = new PropertyLoader().withDefaultConfig();

        //loads: "props.properties", "props.$hostname.properties", "props.$user.properties"
        Properties properties = propertyLoader.load("props")
```

Advanced Configuration
----------------------

####1. Search Locations
####2. Suffixes

Processing Features
-------------------

####1. Variable Resolving
####2. Includes
####3. Decryption


Usage example
-------------

Java Doc
--------

Full Java Doc of the code can be found here http://tng.github.io/property-loader/
