---
title: "Метод Aspose::Words::Font::get_UnderlineColor"
linktitle: "get_UnderlineColor"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_UnderlineColor. Получает или задает цвет подчеркивания, применяемого к шрифту, в C++."
type: docs
weight: 56000
url: /ru/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


Получает или задает цвет подчеркивания, применяемого к шрифту.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## Примеры



Показывает, как настроить стиль и цвет подчеркивания текста.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
