---
title: Story.AppendParagraph
second_title: Aspose.Words för .NET API Referens
description: Story metod. En genvägsmetod som skapar enParagraph objekt med valfri text och lägger till den i slutet av detta objekt.
type: docs
weight: 60
url: /sv/net/aspose.words/story/appendparagraph/
---
## Story.AppendParagraph method

En genvägsmetod som skapar en[`Paragraph`](../../paragraph/) objekt med valfri text och lägger till den i slutet av detta objekt.

```csharp
public Paragraph AppendParagraph(string text)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| text | String | Texten till stycket. Kan vara`null` eller tom sträng. |

### Returvärde

Det nyskapade och bifogade stycket.

### Exempel

Visar hur man skapar ett sidhuvud och en sidfot.

```csharp
Document doc = new Document();

// Skapa en rubrik och lägg till ett stycke till den. Texten i det stycket
// kommer att visas överst på varje sida i det här avsnittet, ovanför huvudtexten.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Skapa en sidfot och lägg till ett stycke till den. Texten i det stycket
// kommer att visas längst ned på varje sida i det här avsnittet, under huvudtexten.
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

* class [Paragraph](../../paragraph/)
* class [Story](../)
* namnutrymme [Aspose.Words](../../story/)
* hopsättning [Aspose.Words](../../../)


