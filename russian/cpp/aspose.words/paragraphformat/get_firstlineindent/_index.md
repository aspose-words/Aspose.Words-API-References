---
title: "Метод Aspose::Words::ParagraphFormat::get_FirstLineIndent"
linktitle: "get_FirstLineIndent"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ParagraphFormat::get_FirstLineIndent. Получает или задаёт значение (в пунктах) для отступа первой строки или висячего отступа. Используйте положительные значения для установки отступа первой строки и отрицательные значения для установки висячего отступа в C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


Получает или задает значение (в пунктах) для первого абзацного отступа или висячего отступа. Используйте положительные значения для установки первого абзацного отступа и отрицательные значения для установки висячего отступа.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
