---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat метод"
linktitle: "get_ApplyParagraphFormat"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat метод. Форматирование абзацев, применяемое к новому содержимому в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.replacing/findreplaceoptions/get_applyparagraphformat/
---
## FindReplaceOptions::get_ApplyParagraphFormat method


[Paragraph](../../../aspose.words/paragraph/) formatting applied to new content.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::Replacing::FindReplaceOptions::get_ApplyParagraphFormat() const
```


## Примеры



Показывает, как добавить форматирование к абзацам, в которых операция поиска и замены нашла совпадения.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Every paragraph that ends with a full stop like this one will be right aligned.");
builder->Writeln(u"This one will not!");
builder->Write(u"This one also will.");

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

// Мы можем использовать объект "FindReplaceOptions" для изменения процесса поиска и замены.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Установите свойство "Alignment" в значение "ParagraphAlignment.Right", чтобы выровнять каждый абзац по правому краю.
// которые содержат совпадение, найденное операцией поиска и замены.
options->get_ApplyParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Замените каждую точку, стоящую непосредственно перед разрывом абзаца, на восклицательный знак.
int32_t count = doc->get_Range()->Replace(u".&p", u"!&p", options);

ASSERT_EQ(2, count);
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());
ASSERT_EQ(System::String(u"Every paragraph that ends with a full stop like this one will be right aligned!\r") + u"This one will not!\r" + u"This one also will!", doc->GetText().Trim());
```

## См. также

* Class [ParagraphFormat](../../../aspose.words/paragraphformat/)
* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
