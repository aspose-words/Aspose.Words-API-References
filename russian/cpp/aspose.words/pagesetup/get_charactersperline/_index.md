---
title: "Aspose::Words::PageSetup::get_CharactersPerLine метод"
linktitle: "get_CharactersPerLine"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_CharactersPerLine метод. Получает или задает количество символов в строке в сетке документа в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


Получает или задает количество символов в строке сетки документа.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## Примечания


Минимальное значение свойства равно 1. Максимальное значение зависит от ширины страницы и размера шрифта стиля Normal. Минимальный шаг символов составляет 90 процентов от размера шрифта. Например, максимальное количество символов в строке на странице Letter с полями в один дюйм равно 43.

По умолчанию свойство имеет значение, при котором шаг символов равен размеру шрифта стиля Normal.

## Примеры



Показывает, как задать значение для количества символов, которое может содержать каждая строка.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Включите выравнивание, а затем используйте его, чтобы задать количество символов в строке в этом разделе.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// Количество символов также зависит от размера шрифта.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```

## См. также

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
