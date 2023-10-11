---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Anger om textrutor fotnoter och slutnoter ska inkluderas i statistiken över antalet ord.
type: docs
weight: 220
url: /sv/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Anger om textrutor, fotnoter och slutnoter ska inkluderas i statistiken över antalet ord.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

### Exempel

Visar hur man inkluderar eller utesluter textrutor, fotnoter och slutnoter från statistik för ordräkning.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// Som standard är alternativet inställt på 'false'.
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
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


