---
title: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method"
linktitle: "get_AddBidiMarks"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks метод. Указывает, следует ли добавлять двунаправленные метки перед каждым BiDi‑фрагментом при экспорте в формат простого текста. Значение по умолчанию — false в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


Указывает, следует ли добавлять двунаправленные метки перед каждым BiDi‑блоком при экспорте в формат простого текста. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## Примеры



Показывает, как вставить Unicode‑символ 'RIGHT-TO-LEFT MARK' (U+200F) перед каждым двунаправленным [Run](../../../aspose.words/run/) в тексте.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ сохранения документа в простой текст.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// Установите свойство "AddBidiMarks" в "true", чтобы добавить метки перед фрагментами
// с правосторонним текстом, чтобы указать этот факт.
// Установите свойство "AddBidiMarks" в "false", чтобы записывать весь текст слева направо
// и правосторонние фрагменты одинаково без указания, какой из них какой.
saveOptions->set_AddBidiMarks(addBidiMarks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt", saveOptions);

System::String docText = System::Text::Encoding::get_Unicode()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    ASSERT_EQ(u"\ufeffHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    ASSERT_TRUE(docText.Contains(u"\u200f"));
}
else
{
    ASSERT_EQ(u"\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    ASSERT_FALSE(docText.Contains(u"\u200f"));
}
```

## См. также

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
