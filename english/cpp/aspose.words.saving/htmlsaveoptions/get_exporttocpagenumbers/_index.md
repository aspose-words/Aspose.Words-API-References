---
title: get_ExportTocPageNumbers
second_title: Aspose.Words for C++ API Reference
description: Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is false.
type: docs
weight: 352
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


Specifies whether to write page numbers to table of contents when saving HTML, MHTML and EPUB. Default value is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## Examples



Shows how to display page numbers when saving a document with a table of contents to .html. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a table of contents, and then populate the document with paragraphs formatted using a "Heading"
// style that the table of contents will pick up as entries. Each entry will display the heading paragraph on the left,
// and the page number that contains the heading on the right.
auto fieldToc = System::DynamicCast<FieldToc>(builder->InsertField(FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// HTML documents do not have pages. If we save this document to HTML,
// the page numbers that our TOC displays will have no meaning.
// When we save the document to HTML, we can pass a SaveOptions object to omit these page numbers from the TOC.
// If we set the "ExportTocPageNumbers" flag to "true",
// each TOC entry will display the heading, separator, and page number, preserving its appearance in Microsoft Word.
// If we set the "ExportTocPageNumbers" flag to "false",
// the save operation will omit both the separator and page number and leave the heading for each entry intact.
auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(
        String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 1</span>" +
        u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; "
        u"-aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 1</span>" + u"</p>"));
}
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
