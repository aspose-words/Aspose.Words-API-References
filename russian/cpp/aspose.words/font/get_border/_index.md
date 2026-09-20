---
title: "Метод Aspose::Words::Font::get_Border"
linktitle: "get_Border"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Border. Возвращает объект Border, который определяет границу для шрифта в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/font/get_border/
---
## Font::get_Border method


Возвращает объект [Border](../../border/), который определяет границу для шрифта.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::Font::get_Border()
```


## Примеры



Показывает, как вставить строку, окружённую границей, в документ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```

## См. также

* Class [Border](../../border/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
