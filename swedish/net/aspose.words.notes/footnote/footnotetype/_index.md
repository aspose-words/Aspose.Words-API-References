---
title: Footnote.FootnoteType
second_title: Aspose.Words för .NET API Referens
description: Footnote fast egendom. Returnerar ett värde som anger om detta är en fotnot eller slutnot.
type: docs
weight: 20
url: /sv/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Returnerar ett värde som anger om detta är en fotnot eller slutnot.

```csharp
public FootnoteType FootnoteType { get; }
```

### Exempel

Visar skillnaden mellan fotnoter och slutnoter.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan finns två sätt att bifoga numrerade referenser till texten. Båda dessa referenser kommer att lägga till en
// liten upphöjd referensmarkering på platsen där vi infogar dem.
// Referensmärket är som standard referensens indexnummer bland alla referenser i dokumentet.
// Varje referens kommer också att skapa en post, som kommer att ha samma referensmärke som i brödtexten
// och referenstext, som vi skickar till dokumentbyggarens "InsertFootnote"-metod.
// 1 - En fotnot, vars post kommer att visas på samma sida som texten som den refererar till:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - En slutnot, vars post kommer att visas i slutet av dokumentet:
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
* namnutrymme [Aspose.Words.Notes](../../footnote/)
* hopsättning [Aspose.Words](../../../)


