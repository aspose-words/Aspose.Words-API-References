---
title: Aspose::Words::LineSpacingRule enum
linktitle: LineSpacingRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LineSpacingRule enum. Specifies line spacing values for a paragraph in C++.'
type: docs
weight: 95000
url: /cpp/aspose.words/linespacingrule/
---
## LineSpacingRule enum


Specifies line spacing values for a paragraph.

```cpp
enum class LineSpacingRule
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AtLeast | 0 | The line spacing can be greater than or equal to, but never less than, the value specified in the [LineSpacing](../paragraphformat/get_linespacing/) property. |
| Exactly | 1 | The line spacing never changes from the value specified in the [LineSpacing](../paragraphformat/get_linespacing/) property, even if a larger font is used within the paragraph. |
| Multiple | 2 | The line spacing is specified in the [LineSpacing](../paragraphformat/get_linespacing/) property as the number of lines. One line equals 12 points. |


## Examples



Shows how to work with line spacing. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Below are three line spacing rules that we can define using the
// paragraph's "LineSpacingRule" property to configure spacing between paragraphs.
// 1 -  Set a minimum amount of spacing.
// This will give vertical padding to lines of text of any size
// that is too small to maintain the minimum line-height.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::AtLeast);
builder->get_ParagraphFormat()->set_LineSpacing(20);

builder->Writeln(u"Minimum line spacing of 20.");
builder->Writeln(u"Minimum line spacing of 20.");

// 2 -  Set exact spacing.
// Using font sizes that are too large for the spacing will truncate the text.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Exactly);
builder->get_ParagraphFormat()->set_LineSpacing(5);

builder->Writeln(u"Line spacing of exactly 5.");
builder->Writeln(u"Line spacing of exactly 5.");

// 3 -  Set spacing as a multiple of default line spacing, which is 12 points by default.
// This kind of spacing will scale to different font sizes.
builder->get_ParagraphFormat()->set_LineSpacingRule(Aspose::Words::LineSpacingRule::Multiple);
builder->get_ParagraphFormat()->set_LineSpacing(18);

builder->Writeln(u"Line spacing of 1.5 default lines.");
builder->Writeln(u"Line spacing of 1.5 default lines.");

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.LineSpacing.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
