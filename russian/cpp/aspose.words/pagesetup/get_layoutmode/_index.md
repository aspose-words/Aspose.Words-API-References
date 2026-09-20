---
title: "Метод Aspose::Words::PageSetup::get_LayoutMode"
linktitle: "get_LayoutMode"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_LayoutMode метод. Получает или задает режим макета этого раздела в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words/pagesetup/get_layoutmode/
---
## PageSetup::get_LayoutMode method


Получает или задает режим макета этого раздела.

```cpp
Aspose::Words::SectionLayoutMode Aspose::Words::PageSetup::get_LayoutMode()
```


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

* Enum [SectionLayoutMode](../../sectionlayoutmode/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
