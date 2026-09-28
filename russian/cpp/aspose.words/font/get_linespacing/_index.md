---
title: "Метод Aspose::Words::Font::get_LineSpacing"
linktitle: "get_LineSpacing"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Font::get_LineSpacing. Возвращает межстрочный интервал этого шрифта (в пунктах) в C++."
type: docs
weight: 21000
url: /ru/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


Возвращает межстрочный интервал этого шрифта (в пунктах).

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## Примеры



Показывает, как получить межстрочный интервал шрифта, в пунктах.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите разные шрифты для DocumentBuilder и проверьте их межстрочный интервал.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## См. также

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
