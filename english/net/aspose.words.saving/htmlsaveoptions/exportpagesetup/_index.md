---
title: HtmlSaveOptions.ExportPageSetup
linktitle: ExportPageSetup
articleTitle: ExportPageSetup
second_title: Aspose.Words for .NET
description: Discover how the HtmlSaveOptions ExportPageSetup property enhances your HTML, MHTML, or EPUB exports by allowing customizable page setups for better output.
type: docs
weight: 220
url: /net/aspose.words.saving/htmlsaveoptions/exportpagesetup/
---
## HtmlSaveOptions.ExportPageSetup property

Specifies whether page setup is exported to HTML, MHTML or EPUB. Default is `false`.

```csharp
public bool ExportPageSetup { get; set; }
```

## Remarks

Each [`Section`](../../../aspose.words/section/) in Aspose.Words document model provides page setup information via [`PageSetup`](../../../aspose.words/pagesetup/) class. When you export a document to HTML format you might need to keep this information for further usage. In particular, page setup might be important for rendering to paged media (printing) or subsequent conversion to the native Microsoft Word file formats (DOCX, DOC, RTF, WML).

In most cases HTML is intended for viewing in browsers where pagination is not performed. So this feature is inactive by default.

## Examples

Shows how decide whether to preserve section structure/page setup information when saving to HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TopMargin = 36.0;
pageSetup.BottomMargin = 36.0;
pageSetup.PaperSize = PaperSize.A5;

// When saving the document to HTML, we can pass a SaveOptions object
// to decide whether to preserve or discard page setup settings.
// If we set the "ExportPageSetup" flag to "true", the output HTML document will contain our page setup configuration.
// If we set the "ExportPageSetup" flag to "false", the save operation will discard our page setup settings
// for the first section, and both sections will look identical.
HtmlSaveOptions options = new HtmlSaveOptions { ExportPageSetup = exportPageSetup };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportPageSetup.html");

if (exportPageSetup)
{
    Assert.That(outDocContents.Contains(
        "<style type=\"text/css\">" +
            "@page Section_1 { size:419.55pt 595.3pt; margin:36pt 70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "@page Section_2 { size:612pt 792pt; margin:70.85pt; -aw-footer-distance:35.4pt; -aw-header-distance:35.4pt }" +
            "div.Section_1 { page:Section_1 }div.Section_2 { page:Section_2 }" +
        "</style>"), Is.True);

    Assert.That(outDocContents.Contains(
        "<div class=\"Section_1\">" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"), Is.True);
}
else
{
    Assert.That(outDocContents.Contains("style type=\"text/css\">"), Is.False);

    Assert.That(outDocContents.Contains(
        "<div>" +
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<span>Section 1</span>" +
            "</p>" +
        "</div>"), Is.True);
}
```

### See Also

* class [HtmlSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
