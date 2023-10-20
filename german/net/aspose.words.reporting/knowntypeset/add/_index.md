---
title: KnownTypeSet.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: KnownTypeSet Add methode. Fügt das angegebene hinzuType Objekt zur Menge. WürfeArgumentException in die folgenden Fälle in C#.
type: docs
weight: 20
url: /de/net/aspose.words.reporting/knowntypeset/add/
---
## KnownTypeSet.Add method

Fügt das angegebene hinzuType Objekt zur Menge. WürfeArgumentException in die folgenden Fälle:

-*type* Ist`Null`.

-*type* stellt einen Void-Typ dar.

-*type* stellt einen unsichtbaren Typ dar, dh einen nicht öffentlichen Typ oder einen öffentlichen verschachtelten Typ , der einen nicht öffentlichen äußeren Typ hat.

-*type* stellt einen generischen Typ dar.

-*type* stellt einen Array-Typ dar.

-*type* wurde dem Set bereits hinzugefügt.

```csharp
public void Add(Type type)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| type | Type | AType Objekt, das hinzugefügt werden soll. |

### Siehe auch

* class [KnownTypeSet](../)
* namensraum [Aspose.Words.Reporting](../../../aspose.words.reporting/)
* Montage [Aspose.Words](../../../)
