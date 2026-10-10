---
title: "Método Aspose::Words::Font::get_LineSpacing"
linktitle: "get_LineSpacing"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_LineSpacing. Devuelve el interlineado de esta fuente (en puntos) en C++."
type: docs
weight: 21000
url: /es/cpp/aspose.words/font/get_linespacing/
---
## Font::get_LineSpacing method


Devuelve el interlineado de esta fuente (en puntos).

```cpp
double Aspose::Words::Font::get_LineSpacing()
```


## Ejemplos



Muestra cómo obtener el interlineado de una fuente, en puntos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establece diferentes fuentes para el DocumentBuilder y verifica su interlineado.
builder->get_Font()->set_Name(u"Calibri");
ASPOSE_ASSERT_EQ(14.6484375, builder->get_Font()->get_LineSpacing());

builder->get_Font()->set_Name(u"Times New Roman");
ASPOSE_ASSERT_EQ(13.798828125, builder->get_Font()->get_LineSpacing());
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
