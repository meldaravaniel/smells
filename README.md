# smells
Things you shouldn't do in code.

These are all real-life, production code examples I've found.

## Cyber Boolean
crimes against boolean zen

* `return null == entity ? null : entity;`
* ```
  if (entity != null) {
    return entity;
  } else {
    return null;
  }
```
* ```
System.setProperty("flyway.url", databaseUrl);

if (databaseUrl == null || databaseUrl == null) {...}
```
  * this one gets bonus points because System.setProperty throws a NPE if value OR key are null.  A++
