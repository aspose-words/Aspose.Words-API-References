---
title: "Метод Aspose::Words::ParagraphFormat::get_SnapToGrid"
linktitle: "get_SnapToGrid"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::ParagraphFormat::get_SnapToGrid. Указывает, следует ли текущему абзацу использовать настройки сетки документа по страницам при размещении содержимого абзаца в C++."
type: docs
weight: 30000
url: /ru/cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


Указывает, следует ли текущему абзацу использовать настройки линий сетки документа на страницу при размещении содержимого в абзаце.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
