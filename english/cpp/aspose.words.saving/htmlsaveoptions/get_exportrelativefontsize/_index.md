---
title: get_ExportRelativeFontSize
second_title: Aspose.Words for C++ API Reference
description: Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is false.
type: docs
weight: 300
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportrelativefontsize/
---
## HtmlSaveOptions.get_ExportRelativeFontSize method


Specifies whether font sizes should be output in relative units when saving to HTML, MHTML or EPUB. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize() const
```


In many existing documents (HTML, IDPF EPUB) font sizes are specified in relative units. This allows applications to adjust text size when viewing/processing documents. For instance, Microsoft Internet Explorer has "View->Text Size" submenu, Adobe Digital Editions has two buttons: Increase/Decrease Text Size. If you expect this functionality to work then set [ExportRelativeFontSize](./) property to **true**.

**Aspose**[Words](../../../aspose.words/) document model contains and operates only with absolute font size units. Relative units need additional logic to be recalculated from some initial (standard) size. [Font](../../../aspose.words/font/) size of **Normal** document style is taken as standard. For instance, if **Normal** has 12pt font and some text is 18pt then it will be output as **%1.5em.** to the HTML.

When this option is enabled, document elements other than text will still have absolute sizes. Also some text-related attributes might be expressed absolutely. In particular, line spacing specified with "exactly" rule might produce unwanted results when scaling text. So the source documents should be properly designed and tested when exporting with [ExportRelativeFontSize](./) set to **true**.

## Examples




Shows how to use relative font sizes when saving to .html. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Default font size, ");
builder->get_Font()->set_Size(24);
builder->Writeln(u"2x default font size,");
builder->get_Font()->set_Size(96);
builder->Write(u"8x default font size");

// When we save the document to HTML, we can pass a SaveOptions object
// to determine whether to use relative or absolute font sizes.
// Set the "ExportRelativeFontSize" flag to "true" to declare font sizes
// using the "em" measurement unit, which is a factor that multiplies the current font size.
// Set the "ExportRelativeFontSize" flag to "false" to declare font sizes
// using the "pt" measurement unit, which is the font's absolute size in points.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportRelativeFontSize(exportRelativeFontSize);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.RelativeFontSize.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    ASSERT_TRUE(outDocContents.Contains(String(u"<body style=\"font-family:'Times New Roman'\">") + u"<div>" +
                                        u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" +
                                        u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" + u"<span>2x default font size,</span>" +
                                        u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                                        u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(String(u"<body style=\"font-family:'Times New Roman'; font-size:12pt\">") + u"<div>" +
                                        u"<p style=\"margin-top:0pt; margin-bottom:0pt\">" + u"<span>Default font size, </span>" + u"</p>" +
                                        u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" + u"<span>2x default font size,</span>" +
                                        u"</p>" + u"<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                                        u"<span>8x default font size</span>" + u"</p>" + u"</div>" + u"</body>"));
}
```

