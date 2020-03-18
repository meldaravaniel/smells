# smells
Things you shouldn't do in code.

These are all real-life, production code examples I've found.

## Cyber Boolean
crimes against boolean zen

* `return null == entity ? null : entity;`
* `
  if (entity != null) {
    return entity;
  } else {
    return null;
  }`
