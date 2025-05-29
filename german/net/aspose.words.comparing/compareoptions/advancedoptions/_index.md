---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die erweiterten Optionen von CompareOptions, um Ihre Vergleiche zu verbessern. Erzielen Sie präzise Ergebnisse mit maßgeschneiderten Einstellungen für optimale Ergebnisse.
type: docs
weight: 20
url: /de/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

Gibt erweiterte Vergleichsoptionen an, die zu einer präziseren Vergleichsausgabe beitragen können.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

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

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* namensraum [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Montage [Aspose.Words](../../../)
