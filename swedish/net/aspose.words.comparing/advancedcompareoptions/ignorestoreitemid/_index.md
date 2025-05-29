---
title: AdvancedCompareOptions.IgnoreStoreItemId
linktitle: IgnoreStoreItemId
articleTitle: IgnoreStoreItemId
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen AdvancedCompareOptions IgnoreStoreItemId förbättrar dokumentjämförelse genom att ignorera skillnader i StructuredDocumentTag ID för förbättrad noggrannhet.
type: docs
weight: 30
url: /sv/net/aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/
---
## AdvancedCompareOptions.IgnoreStoreItemId property

Anger om skillnaden i StructuredDocumentTag-lagrets objekt-ID ska ignoreras.

```csharp
public bool IgnoreStoreItemId { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar hur man jämför SDT med samma innehåll men olika artikel-ID i butiken.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Konfigurera alternativ för att jämföra SDT med samma innehåll men olika artikel-ID i butiken.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Se även

* class [AdvancedCompareOptions](../)
* namnutrymme [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* hopsättning [Aspose.Words](../../../)
