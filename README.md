# smells
Things you shouldn't do in code.

These are all real-life, production code examples I've found.

## Testing

```
// dev level: senior.  Seriously, though?  WHY EVEN FEKKIN BOTHER?!?!?!?
package com.package;
import org.junit.Test;

public class CSVUtilitiesTest {


    @Test
    public void test() {

    }

}
```

## Cyber Boolean
crimes against boolean zen

```
// dev level: 3
return null == entity ? null : entity;
```

```
// dev level: 3 (ish?)
return boolCondition ? true : false;
// honestly, what is it with ternaries? why.
```

```
// dev level: architect
  if (entity != null) {
    return entity;
  } else {
    return null;
  }
```

```
/*
  dev level: senior
  
  this one gets bonus points.  Can you tell why?
*/
System.setProperty("flyway.url", databaseUrl);

if (databaseUrl == null || someCondition || databaseUrl == null) {...}
```

```
/* 
   dev level: senior. me. 
   but there's no other way to write it; I was forced to use this API.
   and no.  This isn't java.lang.Boolean.
*/
...(Boolean.builder().withValue(false).build())...
```
