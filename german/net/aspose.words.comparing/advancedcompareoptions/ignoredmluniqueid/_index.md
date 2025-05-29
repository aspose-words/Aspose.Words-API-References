---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words für .NET
description: Entdecken Sie die AdvancedCompareOptions IgnoreDmlUniqueId-Eigenschaft, um Ihre DrawingML-Verarbeitung durch die effiziente Verwaltung eindeutiger IDs zu verbessern. Optimieren Sie Ihren Workflow!
type: docs
weight: 20
url: /de/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

Gibt an, ob Unterschiede in der eindeutigen DrawingML-ID ignoriert werden sollen.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

## Beispiele

Zeigt, wie Dokumente ohne Berücksichtigung der eindeutigen DML-ID verglichen werden.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Standardmäßig ignoriert Aspose.Words die eindeutige ID von DML nicht und die Anzahl der Revisionen betrug 2.
// Wenn wir die eindeutige ID von DML ignorieren und die Anzahl der Revisionen 0 beträgt.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Siehe auch

* class [AdvancedCompareOptions](../)
* namensraum [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Montage [Aspose.Words](../../../)
