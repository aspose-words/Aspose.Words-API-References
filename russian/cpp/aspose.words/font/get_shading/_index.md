---
title: "Метод Aspose::Words::Font::get_Shading"
linktitle: "get_Shading"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Shading. Возвращает объект Shading, который относится к форматированию затенения шрифта в C++."
type: docs
weight: 34000
url: /ru/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


Возвращает объект [Shading](../../shading/), который относится к форматированию затенения для шрифта.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## Примеры



Показывает, как применить затенение к тексту, созданному конструктором документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// Один из способов сделать текст, созданный с использованием нашего белого цвета шрифта, видимым
// это применить эффект фонового затенения.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## См. также

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
