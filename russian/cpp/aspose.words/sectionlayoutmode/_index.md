---
title: "Aspose::Words::SectionLayoutMode перечисление"
linktitle: "SectionLayoutMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::SectionLayoutMode перечисление. Задает режим компоновки секции, позволяющий определить поведение сетки документа в C++."
type: docs
weight: 115000
url: /ru/cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


Указывает режим компоновки раздела, позволяющий определить поведение сетки документа.

```cpp
enum class SectionLayoutMode
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Default | 0 | Указывает, что к содержимому соответствующей секции в документе не будет применяться сетка документа. |
| Grid | 1 | Указывает, что соответствующая секция должна иметь как дополнительный шаг строки, так и шаг символа, добавленные к каждой строке и каждому символу внутри неё, чтобы поддерживать определённое количество строк на страницу и символов в строке. Символы не будут автоматически выравниваться по линиям сетки при вводе. |
| LineGrid | 2 | Указывает, что к каждой строке соответствующей секции будет добавлен дополнительный шаг строки, чтобы поддерживать заданное количество строк на страницу. |
| SnapToChars | 3 | Указывает, что соответствующая секция должна иметь как дополнительный шаг строки, так и шаг символа, добавленные к каждой строке и каждому символу внутри неё, чтобы поддерживать определённое количество строк на страницу и символов в строке. Символы будут автоматически выравниваться по линиям сетки при вводе. |


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


Показывает, как задать ограничение на количество строк, которое может быть на каждой странице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Включите выравнивание, а затем используйте его, чтобы задать количество строк на страницу в этом разделе.
// Достаточно большой размер шрифта перенесёт некоторые строки на следующую страницу, чтобы избежать наложения символов.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
