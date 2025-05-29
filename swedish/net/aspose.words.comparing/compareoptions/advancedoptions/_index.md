---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words för .NET
description: Upptäck CompareOptions AdvancedOptions för att förbättra dina jämförelser. Få exakta resultat med skräddarsydda inställningar för optimalt resultat.
type: docs
weight: 20
url: /sv/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

Anger avancerade jämförelsealternativ som kan bidra till att producera mer exakt jämförelseutdata.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

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

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* namnutrymme [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../../)
