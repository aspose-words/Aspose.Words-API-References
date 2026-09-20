---
title: "Метод Aspose::Words::Font::get_TextEffect"
linktitle: "get_TextEffect"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_TextEffect. Получает или задает эффект анимации шрифта в C++."
type: docs
weight: 47000
url: /ru/cpp/aspose.words/font/get_texteffect/
---
## Font::get_TextEffect method


Получает или задает эффект анимации шрифта.

```cpp
Aspose::Words::TextEffect Aspose::Words::Font::get_TextEffect()
```


## Примеры



Показывает, как применить визуальный эффект к фрагменту.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_TextEffect(Aspose::Words::TextEffect::SparkleText);

builder->Writeln(u"Text with a sparkle effect.");

// Старые версии Microsoft Word поддерживают только эффекты анимации шрифтов.
doc->Save(get_ArtifactsDir() + u"Font.SparklingText.doc");
```

## См. также

* Enum [TextEffect](../../texteffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
