---
title: KnownTypeSet.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for Python
description: "KnownTypeSet.add method. Adds the specified System.Type object to the set"
type: docs
weight: 20
url: /python-net/aspose.words.reporting/knowntypeset/add/
---

## add(type) {#unknown}

Adds the specified System.Type object to the set. Throws System.ArgumentException in
the following cases:

-  is``None``.

-  represents a void type.

-  represents an invisible type, i.e. a non-public type or a public nested type
which has a non-public outer type.

-  represents a generic type.

-  represents an array type.

-  has been added to the set already.




```python
def add(self, type):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| type |  |  |

### See Also

* module [aspose.words.reporting](../../)
* class [KnownTypeSet](../)

