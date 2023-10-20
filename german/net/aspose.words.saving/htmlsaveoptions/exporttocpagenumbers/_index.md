---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: Aspose.Words für .NET
description: HtmlSaveOptions ExportTocPageNumbers eigendom. Gibt an ob beim Speichern von HTML MHTML und EPUB Seitenzahlen in das Inhaltsverzeichnis geschrieben werden sollen. Der Standardwert istFALSCH  in C#.
type: docs
weight: 270
url: /de/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

Gibt an, ob beim Speichern von HTML, MHTML und EPUB Seitenzahlen in das Inhaltsverzeichnis geschrieben werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## Beispiele

Zeigt, wie Seitenzahlen angezeigt werden, wenn ein Dokument mit einem Inhaltsverzeichnis im .html-Format gespeichert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ein Inhaltsverzeichnis einfügen und dann das Dokument mit Absätzen füllen, die mit einer „Überschrift“ formatiert sind.
// Stil, den das Inhaltsverzeichnis als Einträge aufnimmt. Bei jedem Eintrag wird links die Überschrift des Absatzes angezeigt.
// und die Seitenzahl, die rechts die Überschrift enthält.
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

// HTML-Dokumente haben keine Seiten. Wenn wir dieses Dokument im HTML-Format speichern,
// Die Seitenzahlen, die unser Inhaltsverzeichnis anzeigt, haben keine Bedeutung.
// Wenn wir das Dokument im HTML-Format speichern, können wir ein SaveOptions-Objekt übergeben, um diese Seitenzahlen aus dem Inhaltsverzeichnis wegzulassen.
// Wenn wir das Flag „ExportTocPageNumbers“ auf „true“ setzen,
// Jeder Inhaltsverzeichniseintrag zeigt die Überschrift, das Trennzeichen und die Seitenzahl an und behält sein Erscheinungsbild in Microsoft Word bei.
// Wenn wir das Flag „ExportTocPageNumbers“ auf „false“ setzen,
// Beim Speichervorgang werden sowohl das Trennzeichen als auch die Seitenzahl weggelassen und die Überschrift für jeden Eintrag bleibt erhalten.
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

### Siehe auch

* class [HtmlSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
