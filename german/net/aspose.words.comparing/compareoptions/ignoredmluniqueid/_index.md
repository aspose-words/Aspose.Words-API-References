---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Aspose.Words für .NET-API-Referenz
description: CompareOptions eigendom. Gibt an ob Unterschiede in der eindeutigen DrawingMLID ignoriert werden sollen. Der Standardwert istFALSCH .
type: docs
weight: 60
url: /de/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

Gibt an, ob Unterschiede in der eindeutigen DrawingML-ID ignoriert werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### Beispiele

Zeigt, wie Dokumente verglichen werden, wobei die eindeutige DML-ID ignoriert wird.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Standardmäßig ignoriert Aspose.Words die eindeutige ID von DML nicht und die Anzahl der Revisionen betrug 2.
// Wenn wir die eindeutige ID von DML ignorieren und die Anzahl der Revisionen 0 beträgt.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Siehe auch

* class [CompareOptions](../)
* namensraum [Aspose.Words.Comparing](../../compareoptions/)
* Montage [Aspose.Words](../../../)


