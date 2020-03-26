# smells
Things you shouldn't do in code.

These are all real-life, production code examples I've found.

## Cyber Boolean
crimes against boolean zen

```
// dev level: 3
return null == entity ? null : entity;
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

