---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words för .NET
description: Optimera ditt dokuments ordantal med egenskapen IncludeTextboxesFootnotesEndnotesInStat. Kontrollera textrutor, fotnoter och slutnoter utan ansträngning!
type: docs
weight: 230
url: /sv/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Anger om textrutor, fotnoter och slutnoter ska inkluderas i ordräkningsstatistiken.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Exempel

Visar hur man inkluderar eller exkluderar textrutor, fotnoter och slutnoter från ordräkningsstatistik.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Som standard är alternativet satt till 'false'.
doc.UpdateWordCount();
// Ord räknas utan textrutor, fotnoter och slutnoter.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Ord räknas med textrutor, fotnoter och slutnoter.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Se även

* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
