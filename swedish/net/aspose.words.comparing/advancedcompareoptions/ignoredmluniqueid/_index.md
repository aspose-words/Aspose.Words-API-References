---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words för .NET
description: Upptäck egenskapen AdvancedCompareOptions IgnoreDmlUniqueId för att förbättra din DrawingML-bearbetning genom att effektivt hantera unika ID:n. Optimera ditt arbetsflöde!
type: docs
weight: 20
url: /sv/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

Anger om skillnaden i DrawingML:s unika ID ska ignoreras.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar hur man jämför dokument utan att DML:s unika ID används.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Som standard ignorerar Aspose.Words inte DML:s unika ID, och antalet revisioner var 2.
// Om vi ignorerar DML:s unika ID och antalet revisioner var 0.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Se även

* class [AdvancedCompareOptions](../)
* namnutrymme [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../../)
