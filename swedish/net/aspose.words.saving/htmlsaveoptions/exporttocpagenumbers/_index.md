---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: Aspose.Words för .NET
description: Kontrollera sidnummer för innehållsförteckning i HTML-, MHTML- och EPUB-exporter med HtmlSaveOptions. Förbättra navigering och användarupplevelse utan ansträngning!
type: docs
weight: 270
url: /sv/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

Anger om sidnummer ska skrivas till innehållsförteckningen när HTML, MHTML och EPUB sparas. Standardvärdet är`falsk` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## Exempel

Visar hur man visar sidnummer när man sparar ett dokument med en innehållsförteckning till .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en innehållsförteckning och fyll sedan dokumentet med stycken formaterade med en "Rubrik"
// stil som innehållsförteckningen kommer att hämta som poster. Varje post kommer att visa rubriken till vänster,
// och sidnumret som innehåller rubriken till höger.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// HTML-dokument har inga sidor. Om vi sparar detta dokument som HTML,
// sidnumren som vår innehållsförteckning visar kommer inte att ha någon betydelse.
// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt för att utelämna dessa sidnummer från innehållsförteckningen.
// Om vi ställer in flaggan "ExportTocPageNumbers" till "sant",
// varje innehållsförteckning visar rubrik, avgränsare och sidnummer, vilket behåller utseendet i Microsoft Word.
// Om vi ställer in flaggan "ExportTocPageNumbers" till "false",
// sparåtgärden utelämnar både avgränsare och sidnummer och lämnar rubriken för varje post intakt.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 2</span>" +
        "</p>"));
}
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
