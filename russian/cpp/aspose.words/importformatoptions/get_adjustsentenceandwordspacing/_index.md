---
title: "Метод Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing"
linktitle: "get_AdjustSentenceAndWordSpacing"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing. Получает или задает логическое значение, указывающее, следует ли автоматически регулировать интервал между предложениями и словами. Значение по умолчанию — false в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/importformatoptions/get_adjustsentenceandwordspacing/
---
## ImportFormatOptions::get_AdjustSentenceAndWordSpacing method


Получает или задает логическое значение, которое указывает, следует ли автоматически регулировать интервалы между предложениями и словами. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AdjustSentenceAndWordSpacing() const
```


## Примеры



Показывает, как автоматически регулировать интервал между предложениями и словами.
```cpp
auto srcDoc = System::MakeObject<Aspose::Words::Document>();
auto dstDoc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(srcDoc);
builder->Write(u"Dolor sit amet.");

builder = System::MakeObject<Aspose::Words::DocumentBuilder>(dstDoc);
builder->Write(u"Lorem ipsum.");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AdjustSentenceAndWordSpacing(true);
builder->InsertDocument(srcDoc, Aspose::Words::ImportFormatMode::UseDestinationStyles, options);

ASSERT_EQ(u"Lorem ipsum. Dolor sit amet.", dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```

## См. также

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
