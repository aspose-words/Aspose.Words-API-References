---
title: Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha method
linktitle: get_AddSpaceBetweenFarEastAndAlpha
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha method. Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/paragraphformat/get_addspacebetweenfareastandalpha/
---
## ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha method


Gets or sets a flag indicating whether inter-character spacing is automatically adjusted between regions of Latin text and regions of East Asian text in the current paragraph.

```cpp
bool Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha()
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
