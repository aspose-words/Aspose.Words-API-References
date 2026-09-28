---
title: "Метод Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation"
linktitle: "get_ListIndentation"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation. Возвращает объект TxtListIndentation, который указывает, сколько и какой символ использовать для отступов уровней списка. По умолчанию используется нулевое количество символа ''\\\\0'', что означает отсутствие отступа в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.saving/txtsaveoptions/get_listindentation/
---
## TxtSaveOptions::get_ListIndentation method


Возвращает объект [TxtListIndentation](../../txtlistindentation/), который указывает, сколько и какой символ использовать для отступов уровней списка. По умолчанию используется нулевое количество символа '\\0', что означает отсутствие отступа.

```cpp
System::SharedPtr<Aspose::Words::Saving::TxtListIndentation> Aspose::Words::Saving::TxtSaveOptions::get_ListIndentation() const
```


## Примеры



Показывает, как настроить отступы списка при сохранении документа в простой текст.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте список с тремя уровнями отступа.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
// чтобы изменить способ сохранения документа в простой текст.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Установите свойство "Character", чтобы задать используемый символ
// для заполнения, имитирующего отступы списка в простом тексте.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Установите свойство "Count", чтобы указать количество раз
// для размещения символа заполнения на каждом уровне отступа списка.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## См. также

* Class [TxtListIndentation](../../txtlistindentation/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
