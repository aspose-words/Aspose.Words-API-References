---
title: "Aspose::Words::ControlChar::Cr метод"
linktitle: "Cr"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ControlChar::Cr метод. Символ возврата каретки: \"\\x000d\" или \"\\r\". То же, что ParagraphBreak в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/controlchar/cr/
---
## ControlChar::Cr method


Символ возврата каретки: "\x000d" или "\r". То же, что [ParagraphBreak](../paragraphbreak/).

```cpp
static System::String & Aspose::Words::ControlChar::Cr()
```


## Примеры



Показывает, как использовать управляющие символы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставка абзацев с текстом с помощью DocumentBuilder.
builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Преобразование документа в текстовый вид показывает, что управляющие символы
// представляют некоторые структурные элементы документа, такие как разрывы страниц.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + System::String::Format(u"Hello again!{0}", Aspose::Words::ControlChar::Cr()) + Aspose::Words::ControlChar::PageBreak(), doc->GetText());

// При преобразовании документа в строковый вид,
// мы можем опустить некоторые управляющие символы с помощью метода Trim.
ASSERT_EQ(System::String::Format(u"Hello world!{0}", Aspose::Words::ControlChar::Cr()) + u"Hello again!", doc->GetText().Trim());
```

## См. также

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
