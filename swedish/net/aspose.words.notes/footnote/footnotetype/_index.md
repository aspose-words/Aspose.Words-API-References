---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FootnoteType, identifiera enkelt fotnoter eller slutnoter i dina dokument för ökad tydlighet och organisation.
type: docs
weight: 30
url: /sv/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Returnerar ett värde som anger om detta är en fotnot eller slutnot.

```csharp
public FootnoteType FootnoteType { get; }
```

## Exempel

Visar skillnaden mellan fotnoter och slutnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer två sätt att koppla numrerade referenser till texten. Båda dessa referenser kommer att lägga till en
// litet upphöjd referensmärke på den plats där vi infogar dem.
// Referensmärket är som standard referensens indexnummer bland alla referenser i dokumentet.
// Varje referens skapar också en post, som får samma referensmarkering som i brödtexten
// och referenstext, som vi skickar till dokumentbyggarens "InsertFootnote"-metod.
// 1 - En fotnot, vars inlägg kommer att visas på samma sida som texten den refererar till:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - En slutnot, vars inlägg kommer att visas i slutet av dokumentet:
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(FootnoteType.Footnote, footnote.FootnoteType);
Assert.AreEqual(FootnoteType.Endnote, endnote.FootnoteType);

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### Se även

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* namnutrymme [Aspose.Words.Notes](../../../aspose.words.notes/)
* hopsättning [Aspose.Words](../../../)
