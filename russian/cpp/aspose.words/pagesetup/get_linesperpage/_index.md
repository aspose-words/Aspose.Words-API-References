---
title: "Aspose::Words::PageSetup::get_LinesPerPage метод"
linktitle: "get_LinesPerPage"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::PageSetup::get_LinesPerPage метод. Получает или задает количество строк на странице в сетке документа в C++."
type: docs
weight: 26000
url: /ru/cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


Получает или задает количество строк на страницу в сетке документа.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## Примечания


Минимальное значение свойства равно 1. Максимальное значение зависит от высоты страницы и размера шрифта стиля Normal. Минимальный шаг строки составляет 136 процентов от размера шрифта. Например, максимальное количество строк на странице формата Letter с одно-дюймовыми полями равно 39.

По умолчанию свойство имеет значение, при котором шаг строки в 1,5 раза больше размера шрифта стиля Normal.

## Примеры



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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
