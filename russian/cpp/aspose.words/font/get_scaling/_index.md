---
title: "Aspose::Words::Font::get_Scaling метод"
linktitle: "get_Scaling"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Font::get_Scaling метод. Получает или задает масштаб ширины символов в процентах в C++."
type: docs
weight: 33000
url: /ru/cpp/aspose.words/font/get_scaling/
---
## Font::get_Scaling method


Получает или задает масштабирование ширины символов в процентах.

```cpp
int32_t Aspose::Words::Font::get_Scaling()
```


## Примеры



Показывает, как установить горизонтальное масштабирование и интервал между символами.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте фрагмент текста и увеличьте ширину символов до 150%.
builder->get_Font()->set_Scaling(150);
builder->Writeln(u"Wide characters");

// Добавьте фрагмент текста и добавьте дополнительный горизонтальный интервал в 1pt между каждым символом.
builder->get_Font()->set_Spacing(1);
builder->Writeln(u"Expanded by 1pt");

// Добавьте фрагмент текста и сблизьте символы друг с другом на 1pt.
builder->get_Font()->set_Spacing(-1);
builder->Writeln(u"Condensed by 1pt");

doc->Save(get_ArtifactsDir() + u"Font.ScalingSpacing.docx");
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
