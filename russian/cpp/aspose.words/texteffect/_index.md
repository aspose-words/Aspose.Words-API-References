---
title: "Aspose::Words::TextEffect enum"
linktitle: "TextEffect"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TextEffect enum. Эффект анимации для текстовых фрагментов в C++."
type: docs
weight: 123000
url: /ru/cpp/aspose.words/texteffect/
---
## TextEffect enum


Эффект анимации для текстовых фрагментов.

```cpp
enum class TextEffect
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 |  |
| LasVegasLights | 1 |  |
| BlinkingBackground | 2 |  |
| SparkleText | 3 |  |
| MarchingBlackAnts | 4 |  |
| MarchingRedAnts | 5 |  |
| Shimmer | 6 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
