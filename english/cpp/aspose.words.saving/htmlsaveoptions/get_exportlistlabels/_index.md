---
title: get_ExportListLabels
second_title: Aspose.Words for C++ API Reference
description: Controls how list labels are output to HTML, MHTML or EPUB. Default value is Auto.
type: docs
weight: 248
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportlistlabels/
---
## HtmlSaveOptions::get_ExportListLabels method


Controls how list labels are output to HTML, MHTML or EPUB. Default value is [Auto](../../exportlistlabels/).

```cpp
Aspose::Words::Saving::ExportListLabels Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels() const
```


## Examples



Shows how to configure list exporting to HTML. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(list);

builder->Writeln(u"Default numbered list item 1.");
builder->Writeln(u"Default numbered list item 2.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Default numbered list item 3.");
builder->get_ListFormat()->RemoveNumbers();

list = doc->get_Lists()->Add(ListTemplate::OutlineHeadingsLegal);
builder->get_ListFormat()->set_List(list);

builder->Writeln(u"Outline legal heading list item 1.");
builder->Writeln(u"Outline legal heading list item 2.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 3.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 4.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 5.");
builder->get_ListFormat()->RemoveNumbers();

// When saving the document to HTML, we can pass a SaveOptions object
// to decide which HTML elements the document will use to represent lists.
// Setting the "ExportListLabels" property to "ExportListLabels.AsInlineText"
// will create lists by formatting spans.
// Setting the "ExportListLabels" property to "ExportListLabels.Auto" will use the <p> tag
// to build lists in cases when using the <ol> and <li> tags may cause loss of formatting.
// Setting the "ExportListLabels" property to "ExportListLabels.ByHtmlTags"
// will use <ol> and <li> tags to build all lists.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportListLabels(exportListLabels);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.List.html", options);
String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.List.html");

switch (exportListLabels)
{
case ExportListLabels::AsInlineText:
    ASSERT_TRUE(outDocContents.Contains(
        String(u"<p style=\"margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; "
               u"-aw-list-number-format:'%1.'; -aw-list-number-styles:'lowerLetter'; -aw-list-number-values:'1'; -aw-list-padding-sml:9.67pt\">") +
        u"<span style=\"-aw-import:ignore\">" + u"<span>a.</span>" +
        u"<span style=\"width:9.67pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; "
        u"</span>" +
        u"</span>" + u"<span>Default numbered list item 3.</span>" + u"</p>"));
    ASSERT_TRUE(
        outDocContents.Contains(String(u"<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; "
                                       u"-aw-list-level-number:3; -aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal "
                                       u"decimal decimal'; -aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">") +
                                u"<span style=\"-aw-import:ignore\">" + u"<span>2.1.1.1</span>" +
                                u"<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; "
                                u"-aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                                u"</span>" + u"<span>Outline legal heading list item 5.</span>" + u"</p>"));
    break;

case ExportListLabels::Auto:
    ASSERT_TRUE(outDocContents.Contains(String(u"<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">") +
                                        u"<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" + u"<span>Default numbered list item 3.</span>" +
                                        u"</li>" + u"</ol>"));
    ASSERT_TRUE(outDocContents.Contains(
        String(
            u"<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; ") +
        u"-aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal decimal decimal'; " +
        u"-aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">" + u"<span style=\"-aw-import:ignore\">" + u"<span>2.1.1.1</span>" +
        u"<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; "
        u"</span>" +
        u"</span>" + u"<span>Outline legal heading list item 5.</span>" + u"</p>"));
    break;

case ExportListLabels::ByHtmlTags:
    ASSERT_TRUE(outDocContents.Contains(String(u"<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">") +
                                        u"<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" + u"<span>Default numbered list item 3.</span>" +
                                        u"</li>" + u"</ol>"));
    ASSERT_TRUE(outDocContents.Contains(String(u"<ol type=\"1\" class=\"awlist3\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">") +
                                        u"<li style=\"margin-left:7.2pt; text-indent:-43.2pt; -aw-list-padding-sml:10.2pt\">" +
                                        u"<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; "
                                        u"-aw-import:ignore\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" +
                                        u"<span>Outline legal heading list item 5.</span>" + u"</li>" + u"</ol>"));
    break;
}
```

## See Also

* Enum [ExportListLabels](../../exportlistlabels/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
