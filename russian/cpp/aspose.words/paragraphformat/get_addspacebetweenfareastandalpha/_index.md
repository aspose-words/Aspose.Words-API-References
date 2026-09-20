---
title: "Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha метод"
linktitle: "get_AddSpaceBetweenFarEastAndAlpha"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha method. Получает или задает флаг, указывающий, автоматически ли регулируется межсимвольный интервал между регионами латинского текста и регионами восточноазиатского текста в текущем абзаце на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/paragraphformat/get_addspacebetweenfareastandalpha/
---
## ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha method


Получает или задаёт флаг, указывающий, автоматически ли регулируется межсимвольный интервал между областями латинского текста и областями восточноазиатского текста в текущем абзаце.

```cpp
bool Aspose::Words::ParagraphFormat::get_AddSpaceBetweenFarEastAndAlpha()
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
