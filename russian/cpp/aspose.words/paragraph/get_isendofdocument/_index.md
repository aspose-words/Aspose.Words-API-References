---
title: "Метод Aspose::Words::Paragraph::get_IsEndOfDocument"
linktitle: "get_IsEndOfDocument"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Paragraph::get_IsEndOfDocument. Истина, если этот абзац является последним абзацем в последнем разделе документа в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/paragraph/get_isendofdocument/
---
## Paragraph::get_IsEndOfDocument method


Истина, если этот абзац является последним абзацем в последнем разделе документа.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfDocument()
```


## Примеры



Показывает, как вставить абзац в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// Метод "Writeln" завершает абзац после добавления текста
// а затем начинается новая строка, добавляя новый абзац.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## См. также

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
