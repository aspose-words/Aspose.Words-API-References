---
title: ExportListLabels Enum
linktitle: ExportListLabels
articleTitle: ExportListLabels
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Saving.ExportListLabels-enumet förbättrar dina HTML-, MHTML- och EPUB-exporter med anpassningsbara listetikettalternativ.
type: docs
weight: 5760
url: /sv/net/aspose.words.saving/exportlistlabels/
---
## ExportListLabels enumeration

Anger hur listetiketter exporteras till HTML, MHTML och EPUB.

```csharp
public enum ExportListLabels
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Visar listade etiketter i autoläge. Använder HTML-element när det är möjligt. |
| AsInlineText | `1` | Visar alla listetiketter som inbäddad text. |
| ByHtmlTags | `2` | Matar ut alla listetiketter som HTML-element. |

## Exempel

Visar hur man konfigurerar export av listor till HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Aspose.Words.Lists.List list = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = list;

builder.Writeln("Default numbered list item 1.");
builder.Writeln("Default numbered list item 2.");
builder.ListFormat.ListIndent();
builder.Writeln("Default numbered list item 3.");
builder.ListFormat.RemoveNumbers();

list = doc.Lists.Add(ListTemplate.OutlineHeadingsLegal);
builder.ListFormat.List = list;

builder.Writeln("Outline legal heading list item 1.");
builder.Writeln("Outline legal heading list item 2.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 3.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 4.");
builder.ListFormat.ListIndent();
builder.Writeln("Outline legal heading list item 5.");
builder.ListFormat.RemoveNumbers();

// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma vilka HTML-element dokumentet ska använda för att representera listor.
// Ställer in egenskapen "ExportListLabels" till "ExportListLabels.AsInlineText"
// skapar listor genom att formatera spann.
// Om egenskapen "ExportListLabels" ställs in på "ExportListLabels.Auto" används taggen <p>
// att bygga listor i de fall då användning av taggarna <ol> och <li> kan orsaka formateringsförlust.
// Ställer in egenskapen "ExportListLabels" till "ExportListLabels.ByHtmlTags"
// kommer att använda taggarna <ol> och <li> för att bygga alla listor.
HtmlSaveOptions options = new HtmlSaveOptions { ExportListLabels = exportListLabels };

doc.Save(ArtifactsDir + "HtmlSaveOptions.List.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.List.html");

switch (exportListLabels)
{
    case ExportListLabels.AsInlineText:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; -aw-list-number-format:'%1.'; -aw-list-number-styles:'lowerLetter'; -aw-list-number-values:'1'; -aw-list-padding-sml:9.67pt\">" +
                "<span style=\"-aw-import:ignore\">" +
                    "<span>a.</span>" +
                    "<span style=\"width:9.67pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                "</span>" +
                "<span>Default numbered list item 3.</span>" +
            "</p>"));

        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; -aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal decimal decimal'; -aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">" +
                "<span style=\"-aw-import:ignore\">" +
                    "<span>2.1.1.1</span>" +
                    "<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                "</span>" +
                "<span>Outline legal heading list item 5.</span>" +
            "</p>"));
        break;
    case ExportListLabels.Auto:
        Assert.True(outDocContents.Contains(
            "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
                "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
                    "<span>Default numbered list item 3.</span>" +
                "</li>" +
            "</ol>"));
        break;
    case ExportListLabels.ByHtmlTags:
        Assert.True(outDocContents.Contains(
            "<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">" +
                "<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" +
                    "<span>Default numbered list item 3.</span>" +
                "</li>" +
            "</ol>"));
        break;
}
```

### Se även

* property [ExportListLabels](../htmlsaveoptions/exportlistlabels/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
