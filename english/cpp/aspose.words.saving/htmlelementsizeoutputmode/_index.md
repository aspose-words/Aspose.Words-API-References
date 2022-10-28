---
title: HtmlElementSizeOutputMode
second_title: Aspose.Words for C++ API Reference
description: Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB.
type: docs
weight: 742
url: /cpp/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enum


Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB.

### Values

| Name | Value | Description |
| --- | --- | --- |
| All | 0 | All element sizes, both in absolute and relative units, specified in the document are exported. |
| RelativeOnly | 1 | Element sizes are exported only if they are specified in relative units in the document. Fixed sizes are not exported in this mode. Visual agents will calculate missing sizes to make document layout more natural. |
| None | 2 | Element sizes are not exported. Visual agents will build layout automatically according to relationship between elements. |


## Examples




Shows how to preserve negative indents in the output .html. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Insert a table with a negative indent, which will push it to the left past the left page boundary.
SharedPtr<Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(-36);
table->set_PreferredWidth(PreferredWidth::FromPoints(144));

builder->InsertBreak(BreakType::ParagraphBreak);

// Insert a table with a positive indent, which will push the table to the right.
table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2");
builder->EndTable();
table->set_LeftIndent(36);
table->set_PreferredWidth(PreferredWidth::FromPoints(144));

// When we save a document to HTML, Aspose.Words will only preserve negative indents
// such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
// in a SaveOptions object that we will pass to "true".
auto options = MakeObject<HtmlSaveOptions>(SaveFormat::Html);
options->set_AllowNegativeIndent(allowNegativeIndent);
options->set_TableWidthOutputMode(HtmlElementSizeOutputMode::RelativeOnly);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.NegativeIndent.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    ASSERT_TRUE(outDocContents.Contains(
        u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; "
        u"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(
        u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; "
        u"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    ASSERT_TRUE(
        outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; "
                                u"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    ASSERT_TRUE(outDocContents.Contains(
        u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; "
        u"-aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

