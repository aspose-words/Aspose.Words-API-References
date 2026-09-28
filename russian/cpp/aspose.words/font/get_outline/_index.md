---
title: "Aspose::Words::Font::get_Outline метод"
linktitle: "get_Outline"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Outline. Истина, если шрифт отформатирован как контурный в C++."
type: docs
weight: 31000
url: /ru/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


Истина, если шрифт отформатирован как контур.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## Примеры



Показывает, как создать фрагмент текста, отформатированный как контур.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите флаг Outline, чтобы изменить цвет заливки текста на белый и
// оставить тонкую обводку вокруг каждого символа исходным цветом текста.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
