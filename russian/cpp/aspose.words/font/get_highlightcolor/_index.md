---
title: "Aspose::Words::Font::get_HighlightColor метод"
linktitle: "get_HighlightColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Font::get_HighlightColor метод. Получает или задает цвет выделения (маркировки) в C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


Получает или задаёт цвет выделения (маркер).

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## Примеры



Показывает, как форматировать run текста, используя его свойство font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
