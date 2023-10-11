---
title: ParagraphFormat.PageBreakBefore
second_title: Aspose.Words för .NET API Referens
description: ParagraphFormat fast egendom. Sant om en sidbrytning tvingas före stycket.
type: docs
weight: 260
url: /sv/net/aspose.words/paragraphformat/pagebreakbefore/
---
## ParagraphFormat.PageBreakBefore property

Sant om en sidbrytning tvingas före stycket.

```csharp
public bool PageBreakBefore { get; set; }
```

### Exempel

Visar hur man skapar stycken med sidbrytningar i början.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sätt denna flagga på "true" för att tillämpa en sidbrytning i början av varje stycke
// som dokumentbyggaren kommer att skapa under denna ParagraphFormat-konfiguration.
// Det första stycket kommer inte att få en sidbrytning.
// Lämna denna flagga som "falsk" för att starta varje nytt stycke på samma sida
// som föregående, förutsatt att det finns tillräckligt med utrymme.
builder.ParagraphFormat.PageBreakBefore = pageBreakBefore;

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

LayoutCollector layoutCollector = new LayoutCollector(doc);
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

if (pageBreakBefore)
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(2, layoutCollector.GetStartPageIndex(paragraphs[1]));
}
else
{
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[0]));
    Assert.AreEqual(1, layoutCollector.GetStartPageIndex(paragraphs[1]));
}

doc.Save(ArtifactsDir + "ParagraphFormat.PageBreakBefore.docx");
```

### Se även

* class [ParagraphFormat](../)
* namnutrymme [Aspose.Words](../../paragraphformat/)
* hopsättning [Aspose.Words](../../../)


