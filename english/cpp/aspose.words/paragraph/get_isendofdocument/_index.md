---
title: get_IsEndOfDocument
second_title: Aspose.Words for C++ API Reference
description: True if this paragraph is the last paragraph in the last section of the document.
type: docs
weight: 92
url: /cpp/aspose.words/paragraph/get_isendofdocument/
---
## Paragraph.get_IsEndOfDocument method


True if this paragraph is the last paragraph in the last section of the document.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfDocument()
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

