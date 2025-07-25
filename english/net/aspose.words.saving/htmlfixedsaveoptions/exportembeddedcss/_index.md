---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words for .NET
description: Discover how the ExportEmbeddedCss property of HtmlFixedSaveOptions enhances your HTML documents by embedding CSS for seamless styling. Optimize your web pages today!
type: docs
weight: 40
url: /net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Examples

Shows how to determine where to store CSS stylesheets when exporting a document to Html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// When we export a document to html, Aspose.Words will also create a CSS stylesheet to format the document with.
// Setting the "ExportEmbeddedCss" flag to "true" save the CSS stylesheet to a .css file,
// and link to the file from the html document using a <link> element.
// Setting the flag to "false" will embed the CSS stylesheet within the Html document,
// which will create only one file instead of two.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.That(Regex.Match(outDocContents, "<style type=\"text/css\">").Success, Is.True);
    Assert.That(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"), Is.False);
}
else
{
    Assert.That(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success, Is.True);
    Assert.That(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"), Is.True);
}
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
