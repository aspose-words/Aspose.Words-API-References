---
title: Aspose::Words::ParagraphFormat::get_LineSpacing method
linktitle: get_LineSpacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_LineSpacing method. Gets or sets the line spacing (in points) for the paragraph in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words/paragraphformat/get_linespacing/
---
## ParagraphFormat::get_LineSpacing method


Gets or sets the line spacing (in points) for the paragraph.

```cpp
double Aspose::Words::ParagraphFormat::get_LineSpacing()
```

## Remarks


When [LineSpacingRule](../get_linespacingrule/) property is set to [AtLeast](../../linespacingrule/), the line spacing can be greater than or equal to, but never less than the specified [LineSpacing](./) value.

When [LineSpacingRule](../get_linespacingrule/) property is set to [Exactly](../../linespacingrule/), the line spacing never changes from the specified [LineSpacing](./) value, even if a larger font is used within the paragraph.

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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
