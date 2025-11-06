---
title: Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode method
linktitle: get_TableWidthOutputMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode method. Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is All in C++.'
type: docs
weight: 47000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_tablewidthoutputmode/
---
## HtmlSaveOptions::get_TableWidthOutputMode method


Controls how table, row and cell widths are exported to HTML, MHTML or EPUB. Default value is [All](../../htmlelementsizeoutputmode/).

```cpp
Aspose::Words::Saving::HtmlElementSizeOutputMode Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode() const
```

## Remarks


In the HTML format, table, row and cell elements (**%<table>**, **%<tr>**, **%<th>**, **%<td>**) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.

When you convert a document to HTML using Aspose.Words, you might want to control how table, row and cell widths are exported to affect how the resulting document is displayed in the visual agent (e.g. a browser or viewer).

Use this property as a filter to specify what table widths values are exported into the destination document. For example, if you are converting a document to EPUB and intend to view the document on a mobile reading device, then you probably want to avoid exporting absolute width values. To do this you need to specify the output mode [RelativeOnly](../../htmlelementsizeoutputmode/) or [None](../../htmlelementsizeoutputmode/) so the viewer on the mobile device can layout the table to fit the width of the screen as best as it can.

## Examples



Shows how to preserve negative indents in the output .html. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Insert a table with a negative indent, which will push it to the left past the left page boundary.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

builder->InsertBreak(Aspose::Words::BreakType::ParagraphBreak);

// Insert a table with a positive indent, which will push the table to the right.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(144));

// When we save a document to HTML, Aspose.Words will only preserve negative indents
// such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
// in a SaveOptions object that we will pass to "true".
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(Aspose::Words::Saving::HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

## See Also

* Enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
