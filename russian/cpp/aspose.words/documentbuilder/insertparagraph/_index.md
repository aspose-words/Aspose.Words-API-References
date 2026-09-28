---
title: "Aspose::Words::DocumentBuilder::InsertParagraph метод"
linktitle: "InsertParagraph"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBuilder::InsertParagraph метод. Вставляет разрыв абзаца в документ в C++."
type: docs
weight: 44000
url: /ru/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


Вставляет разрыв абзаца в документ.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

Узел абзаца, который только что был вставлен. Это тот же узел, что и [CurrentParagraph](../get_currentparagraph/).
## Примечания


Используется форматирование текущего абзаца, указанное свойством [ParagraphFormat](../get_paragraphformat/).

Разбивает текущий абзац на два. После вставки абзаца курсор помещается в начало нового абзаца.

Исключение выбрасывается, если невозможно вставить разрыв абзаца в текущей позиции курсора.

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

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
