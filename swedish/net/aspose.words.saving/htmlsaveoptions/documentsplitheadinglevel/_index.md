---
title: HtmlSaveOptions.DocumentSplitHeadingLevel
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger den maximala nivån för rubriker för att dela dokumentet. Standardvärdet är2 .
type: docs
weight: 90
url: /sv/net/aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/
---
## HtmlSaveOptions.DocumentSplitHeadingLevel property

Anger den maximala nivån för rubriker för att dela dokumentet. Standardvärdet är`2` .

```csharp
public int DocumentSplitHeadingLevel { get; set; }
```

### Anmärkningar

När[`DocumentSplitCriteria`](../documentsplitcriteria/) inkluderarHeadingParagraph och den här egenskapen är inställd på ett värde från 1 till 9, kommer dokumentet att delas i stycken formaterade med  **Rubrik 1** , **Rubrik 2** , **Rubrik 3**etc. stilar upp till angiven rubriknivå.

Endast som standard **Rubrik 1** och **Rubrik 2** stycken gör att dokumentet delas. Om du ställer in den här egenskapen till noll kommer dokumentet inte att delas vid rubrikstycken alls.

### Exempel

Visar hur man delar upp ett HTML-dokument efter rubriker i flera delar.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varje stycke som vi formaterar med en "Rubrik"-stil kan fungera som en rubrik.
// Varje rubrik kan också ha en rubriknivå, som bestäms av numret på dess rubrikstil.
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

// Skapa ett HtmlSaveOptions-objekt och ställ in delingskriterierna till "HeadingParagraph".
// Dessa kriterier kommer att dela upp dokumentet i stycken med "Rubrik"-stilar i flera mindre dokument,
// och spara varje dokument i en separat HTML-fil i det lokala filsystemet.
// Vi kommer också att ställa in den maximala rubriknivån, vilket delar upp dokumentet till 2.
// Om du sparar dokumentet delas det upp i rubriker på nivå 1 och 2, men inte på 3 till 9.
HtmlSaveOptions options = new HtmlSaveOptions
{
    DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph,
    DocumentSplitHeadingLevel = 2
};

// Vårt dokument har fyra rubriker på nivåerna 1 - 2. En av dessa rubriker kommer inte att vara det
// en splitpunkt eftersom den är i början av dokumentet.
// Sparandet kommer att dela upp vårt dokument på tre platser, i fyra mindre dokument.
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
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


