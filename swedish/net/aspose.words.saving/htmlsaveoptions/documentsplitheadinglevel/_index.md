---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
linktitle: DocumentSplitHeadingLevel
articleTitle: DocumentSplitHeadingLevel
second_title: Aspose.Words för .NET
description: Optimera dokumentdelning med HtmlSaveOptions DocumentSplitHeadingLevel. Kontrollera rubriknivåer för bättre organisation. Standardinställningen är 2.
type: docs
weight: 90
url: /sv/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Anger den maximala rubriknivån där dokumentet ska delas. Standardvärdet är`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

## Anmärkningar

När[`DocumentSplitCriteria`](../documentsplitcriteria/) inkluderarHeadingParagraph och den här egenskapen är inställd på ett värde från 1 till 9, kommer dokumentet att delas vid stycken formaterade med **Rubrik 1** ,**Rubrik 2** ,**Rubrik 3**etc. stilar upp till den angivna rubriknivån.

Som standard endast**Rubrik 1** och**Rubrik 2** stycken gör att dokumentet delas. Om den här egenskapen ställs in på noll delas dokumentet inte alls vid rubrikstycken.

## Exempel

Visar hur man delar upp ett HTML-dokument med rubriker i flera delar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varje stycke som vi formaterar med formatet "Rubrik" kan fungera som en rubrik.
// Varje rubrik kan också ha en rubriknivå, bestämd av numret på dess rubrikstil.
// Rubrikerna nedan är av nivå 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// Skapa ett HtmlSaveOptions-objekt och sätt delningskriterierna till "HeadingParagraph".
// Dessa kriterier kommer att dela upp dokumentet vid stycken med "Rubrik"-format i flera mindre dokument,
// och spara varje dokument i en separat HTML-fil i det lokala filsystemet.
// Vi kommer också att ställa in den maximala rubriknivån, vilket delar dokumentet till 2.
// Om du sparar dokumentet delas det upp i rubriker på nivå 1 och 2, men inte på nivå 3 till 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Vårt dokument har fyra rubriker på nivå 1–2. En av dessa rubriker kommer inte att vara
// en delningspunkt eftersom den är i början av dokumentet.
// Sparoperationen kommer att dela upp vårt dokument på tre ställen, i fyra mindre dokument.
doc.Save(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html", options);

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels.html");

Assert.AreEqual("Heading #1", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-01.html");

Assert.AreEqual("Heading #2\r" +
                "Heading #3", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-02.html");

Assert.AreEqual("Heading #4", doc.GetText().Trim());

doc = new Document(ArtifactsDir + "HtmlSaveOptions.HeadingLevels-03.html");

Assert.AreEqual("Heading #5\r" +
                "Heading #6", doc.GetText().Trim());
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
