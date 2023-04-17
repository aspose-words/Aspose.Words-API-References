---
title: Aspose::Words::ParagraphFormat::get_FirstLineIndent method
linktitle: get_FirstLineIndent
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_FirstLineIndent method. Gets or sets the value (in points) for a first line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


Gets or sets the value (in points) for a first line or hanging indent. Use positive values to set the first-line indent, and negative values to set the hanging indent.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
```


## Examples



Shows how to insert a paragraph into the document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Underline::Dash);

SharedPtr<ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// The "Writeln" method ends the paragraph after appending text
// and then starts a new line, adding a new paragraph.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
