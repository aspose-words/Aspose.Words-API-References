---
title: ExportListLabels Enum
linktitle: ExportListLabels
articleTitle: ExportListLabels
second_title: Aspose.Words per .NET
description: Scopri come l'enum Aspose.Words.Saving.ExportListLabels migliora le tue esportazioni HTML, MHTML ed EPUB con opzioni di etichette di elenco personalizzabili.
type: docs
weight: 5760
url: /it/net/aspose.words.saving/exportlistlabels/
---
## ExportListLabels enumeration

Specifica come le etichette degli elenchi vengono esportate in HTML, MHTML ed EPUB.

```csharp
public enum ExportListLabels
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Auto | `0` | Emette le etichette degli elenchi in modalità automatica. Utilizza elementi HTML nativi quando possibile. |
| AsInlineText | `1` | Restituisce tutte le etichette degli elenchi come testo in linea. |
| ByHtmlTags | `2` | Restituisce tutte le etichette degli elenchi come elementi nativi HTML. |

## Esempi

Mostra come configurare l'esportazione degli elenchi in HTML.

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

// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per decidere quali elementi HTML il documento utilizzerà per rappresentare gli elenchi.
// Impostazione della proprietà "ExportListLabels" su "ExportListLabels.AsInlineText"
// creerà elenchi formattando gli intervalli.
// Impostando la proprietà "ExportListLabels" su "ExportListLabels.Auto" verrà utilizzato il tag <p>
// per creare elenchi nei casi in cui l'utilizzo dei tag <ol> e <li> potrebbe causare la perdita di formattazione.
// Impostazione della proprietà "ExportListLabels" su "ExportListLabels.ByHtmlTags"
// utilizzerà i tag <ol> e <li> per creare tutti gli elenchi.
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

### Guarda anche

* property [ExportListLabels](../htmlsaveoptions/exportlistlabels/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
