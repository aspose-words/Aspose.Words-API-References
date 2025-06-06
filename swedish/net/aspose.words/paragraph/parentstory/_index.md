---
title: Paragraph.ParentStory
linktitle: ParentStory
articleTitle: ParentStory
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Paragraph ParentStory för att enkelt komma åt artiklar på överordnad sektionsnivå och förbättra dokumentets struktur med alternativ för brödtext eller sidhuvud.
type: docs
weight: 210
url: /sv/net/aspose.words/paragraph/parentstory/
---
## Paragraph.ParentStory property

Hämtar den överordnade artikeln på sektionsnivå som kan vara[`Body`](../../body/) eller[`HeaderFooter`](../../headerfooter/) .

```csharp
public Story ParentStory { get; }
```

## Exempel

Visar hur man skapar ett sidhuvud och en sidfot.

```csharp
Document doc = new Document();

// Skapa en rubrik och lägg till ett stycke i den. Texten i det stycket
// kommer att visas högst upp på varje sida i det här avsnittet, ovanför huvudtexten.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Skapa en sidfot och lägg till ett stycke i den. Texten i det stycket
// kommer att visas längst ner på varje sida i det här avsnittet, under huvudtexten.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Se även

* class [Story](../../story/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
