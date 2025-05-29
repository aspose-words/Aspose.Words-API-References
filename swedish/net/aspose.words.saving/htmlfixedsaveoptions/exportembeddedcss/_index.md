---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen ExportEmbeddedCss i HtmlFixedSaveOptions förbättrar dina HTML-dokument genom att bädda in CSS för sömlös stil. Optimera dina webbsidor idag!
type: docs
weight: 40
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

Anger om CSS (Cascading Style Sheet) ska bäddas in i HTML-dokumentet.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Exempel

Visar hur man avgör var CSS-stilmallar ska lagras när man exporterar ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// När vi exporterar ett dokument till html, kommer Aspose.Words också att skapa ett CSS-stilark att formatera dokumentet med.
// Genom att sätta flaggan "ExportEmbeddedCss" till "true" sparas CSS-stilarket till en .css-fil,
// och länka till filen från html-dokumentet med hjälp av ett <link>-element.
// Om flaggan sätts till "false" bäddas CSS-stilarket in i HTML-dokumentet,
// vilket skapar bara en fil istället för två.
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
