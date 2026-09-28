---
title: "Метод Aspose::Words::Font::get_Shadow"
linktitle: "get_Shadow"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_Shadow. Возвращает true, если шрифт оформлен с тенью в C++."
type: docs
weight: 35000
url: /ru/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


Истина, если шрифт отформатирован как с тенью.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## Примеры



Показывает, как создать фрагмент текста, оформленный с тенью.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите флаг Shadow, чтобы применить смещенный эффект тени,
// делая так, будто буквы плавают над страницей.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
