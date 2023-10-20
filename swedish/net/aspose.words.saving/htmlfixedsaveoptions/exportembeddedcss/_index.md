---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words för .NET
description: HtmlFixedSaveOptions ExportEmbeddedCss fast egendom. Anger om CSS Cascading Style Sheet ska bäddas in i HTMLdokument i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

Anger om CSS (Cascading Style Sheet) ska bäddas in i HTML-dokument.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Exempel

Visar hur man bestämmer var man ska lagra CSS-formatmallar när man exporterar ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// När vi exporterar ett dokument till html kommer Aspose.Words också att skapa en CSS-stilmall att formatera dokumentet med.
// Att ställa in "ExportEmbeddedCss"-flaggan till "true" spara CSS-formatmallen till en .css-fil,
// och länka till filen från html-dokumentet med en <länk> element.
// Att sätta flaggan på "false" kommer att bädda in CSS-formatmallen i HTML-dokumentet,
// som bara skapar en fil istället för två.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
