---
title: "Метод Aspose::Words::Font::get_Italic"
linktitle: "get_Italic"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Italic. True, если шрифт оформлен курсивом в C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


True, если шрифт оформлен курсивом.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## Примеры



Показывает, как написать курсивный текст с помощью DocumentBuilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
