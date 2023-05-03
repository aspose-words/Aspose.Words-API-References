---
title: KnownTypeSet.Add
linktitle: Add
second_title: Aspose.Words for .NET API Reference
description: KnownTypeSet Add method. Adds the specified Type object to the set. Throws ArgumentException in the following cases in C#.
type: docs
weight: 20
url: /net/aspose.words.reporting/knowntypeset/add/
---
## Add method

Adds the specified Type object to the set. Throws ArgumentException in the following cases:

- *type* is `null`.

- *type* represents a void type.

- *type* represents an invisible type, i.e. a non-public type or a public nested type which has a non-public outer type.

- *type* represents a generic type.

- *type* represents an array type.

- *type* has been added to the set already.

```csharp
public void Add(Type type)
```

| Parameter | Type | Description |
| --- | --- | --- |
| type | Type | A Type object to add. |

### See Also

* class [KnownTypeSet](../)
* namespace [Aspose.Words.Reporting](../../knowntypeset/)
* assembly [Aspose.Words](../../../)
