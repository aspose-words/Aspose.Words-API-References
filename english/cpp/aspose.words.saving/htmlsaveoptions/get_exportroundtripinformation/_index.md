---
title: get_ExportRoundtripInformation
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is true for HTML and false for MHTML and EPUB.
type: docs
weight: 313
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportroundtripinformation/
---
## HtmlSaveOptions::get_ExportRoundtripInformation method


Specifies whether to write the roundtrip information when saving to HTML, MHTML or EPUB. Default value is **true** for HTML and **false** for MHTML and EPUB.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation() const
```

## Remarks


[Saving](../../) of the roundtrip information allows to restore document properties such as tab stops, comments, headers and footers during the HTML documents loading back into a [Document](../../../aspose.words/document/) object.

When **true**, the roundtrip information is exported as -aw-* CSS properties of the corresponding HTML elements.

When **false**, causes no roundtrip information to be output into produced files.

## Examples



Shows how to preserve hidden elements when converting to .html. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

// When converting a document to .html, some elements such as hidden bookmarks, original shape positions,
// or footnotes will be either removed or converted to plain text and effectively be lost.
// Saving with a HtmlSaveOptions object with ExportRoundtripInformation set to true will preserve these elements.

// When we save the document to HTML, we can pass a SaveOptions object to determine
// how the saving operation will export document elements that HTML does not support or use,
// such as hidden bookmarks and original shape positions.
// If we set the "ExportRoundtripInformation" flag to "true", the save operation will preserve these elements.
// If we set the "ExportRoundTripInformation" flag to "false", the save operation will discard these elements.
// We will want to preserve such elements if we intend to load the saved HTML using Aspose.Words,
// as they could be of use once again.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportRoundtripInformation(exportRoundtripInformation);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.RoundTripInformation.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.RoundTripInformation.html");
doc = MakeObject<Document>(ArtifactsDir + u"HtmlSaveOptions.RoundTripInformation.html");

if (exportRoundtripInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<div style=\"-aw-headerfooter-type:header-primary; clear:both\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<span style=\"-aw-import:ignore\">&#xa0;</span>"));

    ASSERT_TRUE(outDocContents.Contains(String(u"td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ") +
                                        u"padding-right:2.4pt; padding-left:5.03pt; vertical-align:top; " +
                                        u"-aw-border-bottom:0.5pt single; -aw-border-left:0.5pt single; -aw-border-top:0.5pt single\">"));

    ASSERT_TRUE(outDocContents.Contains(
        u"<li style=\"margin-left:30.2pt; padding-left:5.8pt; -aw-font-family:'Courier New'; -aw-font-weight:normal; -aw-number-format:'o'\">"));

    ASSERT_TRUE(
        outDocContents.Contains(String(u"<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" ") +
                                u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />"));

    ASSERT_TRUE(outDocContents.Contains(String(u"<span>Page number </span>") + u"<span style=\"-aw-field-start:true\"></span>" +
                                        u"<span style=\"-aw-field-code:' PAGE   \\\\* MERGEFORMAT '\"></span>" +
                                        u"<span style=\"-aw-field-separator:true\"></span>" + u"<span>1</span>" +
                                        u"<span style=\"-aw-field-end:true\"></span>"));

    ASSERT_EQ(1, doc->get_Range()->get_Fields()->LINQ_Count([](SharedPtr<Field> f) { return f->get_Type() == FieldType::FieldPage; }));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<div style=\"clear:both\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>&#xa0;</span>"));

    ASSERT_TRUE(
        outDocContents.Contains(String(u"<td colspan=\"2\" style=\"width:210.6pt; border-style:solid; border-width:0.75pt 6pt 0.75pt 0.75pt; ") +
                                u"padding-right:2.4pt; padding-left:5.03pt; vertical-align:top\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<li style=\"margin-left:30.2pt; padding-left:5.8pt\">"));

    ASSERT_TRUE(outDocContents.Contains(u"<img src=\"HtmlSaveOptions.RoundTripInformation.003.jpeg\" width=\"350\" height=\"180\" alt=\"\" />"));

    ASSERT_TRUE(outDocContents.Contains(u"<span>Page number 1</span>"));

    ASSERT_EQ(0, doc->get_Range()->get_Fields()->LINQ_Count([](SharedPtr<Field> f) { return f->get_Type() == FieldType::FieldPage; }));
}
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
