---
title: HtmlSaveOptions.ExportLanguageInformation
linktitle: ExportLanguageInformation
articleTitle: ExportLanguageInformation
second_title: Aspose.Words for .NET
description: Control language export in HTML, MHTML, or EPUB with HtmlSaveOptions. Enhance document accessibility and reach a wider audience effortlessly.
type: docs
weight: 180
url: /net/aspose.words.saving/htmlsaveoptions/exportlanguageinformation/
---
## HtmlSaveOptions.ExportLanguageInformation property

Specifies whether language information is exported to HTML, MHTML or EPUB. Default is `false`.

```csharp
public bool ExportLanguageInformation { get; set; }
```

## Remarks

When this property is set to `true` Aspose.Words outputs **lang** HTML attribute on the document elements that specify language. This can be needed to preserve language related semantics.

## Examples

Shows how to preserve language information when saving to .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use the builder to write text while formatting it in different locales.
builder.Font.LocaleId = new CultureInfo("en-US").LCID;
builder.Writeln("Hello world!");

builder.Font.LocaleId = new CultureInfo("en-GB").LCID;
builder.Writeln("Hello again!");

builder.Font.LocaleId = new CultureInfo("ru-RU").LCID;
builder.Write("Привет, мир!");

// When saving the document to HTML, we can pass a SaveOptions object
// to either preserve or discard each formatted text's locale.
// If we set the "ExportLanguageInformation" flag to "true",
// the output HTML document will contain the locales in "lang" attributes of <span> tags.
// If we set the "ExportLanguageInformation" flag to "false',
// the text in the output HTML document will not contain any locale information.
HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportLanguageInformation = exportLanguageInformation,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    Assert.That(outDocContents.Contains("<span>Hello world!</span>"), Is.True);
    Assert.That(outDocContents.Contains("<span lang=\"en-GB\">Hello again!</span>"), Is.True);
    Assert.That(outDocContents.Contains("<span lang=\"ru-RU\">Привет, мир!</span>"), Is.True);
}
else
{
    Assert.That(outDocContents.Contains("<span>Hello world!</span>"), Is.True);
    Assert.That(outDocContents.Contains("<span>Hello again!</span>"), Is.True);
    Assert.That(outDocContents.Contains("<span>Привет, мир!</span>"), Is.True);
}
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
