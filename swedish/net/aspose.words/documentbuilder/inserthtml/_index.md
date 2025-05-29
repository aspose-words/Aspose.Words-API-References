---
title: DocumentBuilder.InsertHtml
linktitle: InsertHtml
articleTitle: InsertHtml
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med DocumentBuilder InsertHtml-metoden – infoga sömlöst HTML-strängar för dynamisk innehållsintegration.
type: docs
weight: 380
url: /sv/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(*string*) {#inserthtml}

Infogar en HTML-sträng i dokumentet.

```csharp
public void InsertHtml(string html)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| html | String | En HTML-sträng att infoga i dokumentet. |

## Anmärkningar

Du kan använda den här metoden för att infoga ett HTML-fragment eller ett helt HTML-dokument.

## Exempel

Visar hur man använder en dokumentbyggare för att infoga HTML-innehåll i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// Genom att infoga HTML-kod tolkas formateringen av varje element till motsvarande dokumenttextformatering.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

Visar hur man utför en dokumentkoppling med ett anpassat återanrop som hanterar kopplingsdata i form av HTML-dokument.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// Om dokumentkopplingen stöter på ett MERGEFIELD vars namn börjar med prefixet "html_",
/// denna återanropsfunktion tolkar dess sammanslagningsdata som HTML-innehåll och lägger till resultatet till dokumentets plats för MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// Anropas när en dokumentkoppling sammanfogar data till ett MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // Lägg till parsad HTML-data i dokumentets brödtext.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // Eftersom vi redan har infogat det sammanfogade innehållet manuellt,
            // vi behöver inte svara på den här händelsen genom att returnera innehåll via egenskapen "Text".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // Gör ingenting.
    }
}
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertHtml(*string, bool*) {#inserthtml_2}

Infogar en HTML-sträng i dokumentet.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| html | String | En HTML-sträng att infoga i dokumentet. |
| useBuilderFormatting | Boolean | Ett värde som anger om formateringen som anges i[`DocumentBuilder`](../) används som basformatering för text importerad från HTML. |

## Anmärkningar

Du kan använda den här metoden för att infoga ett HTML-fragment eller ett helt HTML-dokument.

När*useBuilderFormatting* är`falsk` , [`DocumentBuilder`](../) Formatering ignoreras och formateringen av infogat text baseras på standard HTML-formatering. Som ett resultat ser texten ut som den renderas i webbläsare.

När*useBuilderFormatting* är`sann` , formatering av infogad text är baserad på[`DocumentBuilder`](../) formatering, och texten ser ut som om den vore infogad med[`Write`](../write/) .

## Exempel

Visar hur man tillämpar formateringen i ett dokumentverktyg när man infogar HTML-innehåll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange en textjustering för verktyget, infoga ett HTML-stycke med en specificerad justering och ett utan.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// Det första stycket har en specificerad justering. När InsertHtml analyserar HTML-koden,
// styckejusteringsvärdet som finns i HTML-koden ersätter alltid dokumentbyggarens värde.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// Det andra stycket har ingen specificerad justering. Det kan få sitt justeringsvärde ifyllt
// av byggarens värde beroende på flaggan vi skickade till InsertHtml-metoden.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertHtml(*string, [HtmlInsertOptions](../../htmlinsertoptions/)*) {#inserthtml_1}

Infogar en HTML-sträng i dokumentet. Gör det möjligt att ange ytterligare alternativ.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| html | String | En HTML-sträng att infoga i dokumentet. |
| options | HtmlInsertOptions | Alternativ som används när HTML-sträng infogas. |

## Anmärkningar

Du kan använda den här metoden för att infoga ett HTML-fragment eller ett helt HTML-dokument.

## Exempel

Visar hur man använder alternativ när man infogar html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// Som standard infogar "DocumentBuilder.InsertHtml" ett HTML-fragment som slutar med ett HTML-element på blocknivå,
// den stänger normalt det blocknivåelementet och infogar en styckebrytning.
// Som ett resultat visas ett nytt tomt stycke efter det infogade dokumentet.
// Om vi anger "HtmlInsertOptions.RemoveLastEmptyParagraph" kommer dessa extra tomma stycken att tas bort.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### Se även

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
