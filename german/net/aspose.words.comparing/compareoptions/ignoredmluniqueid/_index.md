---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Aspose.Words für .NET-API-Referenz
description: CompareOptions eigendom. Gibt an ob der Unterschied in der eindeutigen DrawingMLID ignoriert werden soll. Standardwert ist FALSCH .
type: docs
weight: 50
url: /de/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

Gibt an, ob der Unterschied in der eindeutigen DrawingML-ID ignoriert werden soll. Standardwert ist **FALSCH** .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### Beispiele

Zeigt, wie Dokumente verglichen werden, wobei die eindeutige DML-ID ignoriert wird.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Standardmäßig ignoriert Aspose.Words die eindeutige ID von DML nicht, und die Anzahl der Revisionen war 2.
// Wenn wir die eindeutige ID von DML ignorieren und die Anzahl der Revisionen 0 war.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Siehe auch

* class [CompareOptions](../)
* namensraum [Aspose.Words.Comparing](../../compareoptions/)
* Montage [Aspose.Words](../../../)


