---
title: ReportingEngine.set_restricted_types method
linktitle: set_restricted_types method
articleTitle: set_restricted_types method
second_title: Aspose.Words for Python
description: "ReportingEngine.set_restricted_types method. Specifies types, which members as well as which derived types' members should be inaccessible by the engine through template syntax."
type: docs
weight: 70
url: /python-net/aspose.words.reporting/reportingengine/set_restricted_types/
---

## set_restricted_types(types) {#objectlist}

Specifies types, which members as well as which derived types' members should be inaccessible by the engine
through template syntax.


```python
def set_restricted_types(self, types: List[object]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| types | List[object] | Types to be restricted. |

### Remarks

Restricted types should be set before the very first building of a report. After ``BuildReport`` is invoked, restricted types cannot be modified and an exception is thrown
on attempt to do this. The best place to set restricted types is application startup.


Note that a big amount of restricted types may affect performance, so it is better to restrict only those
types, access to which members is really sensitive.

Throws System.ArgumentException in the following cases:

- *types* is null.

- One of *types* items is``None``.

- One of *types* items represents an invisible type, i.e. a non-public type or
a public nested type which has a non-public outer type.

- One of *types* items represents an array type.

- *types* contain duplicate entries.




### See Also

* module [aspose.words.reporting](../../)
* class [ReportingEngine](../)

