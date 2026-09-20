---
title: "Aspose::Words::Range::get_Text método"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Range::get_Text. Obtiene el texto del rango en C++."
type: docs
weight: 8000
url: /es/cpp/aspose.words/range/get_text/
---
## Range::get_Text method


Obtiene el texto del rango.

```cpp
System::String Aspose::Words::Range::get_Text()
```

## Observaciones


La cadena devuelta incluye todos los caracteres de control y especiales como se describe en [ControlChar](../../controlchar/).

## Ejemplos



Muestra cómo obtener el contenido de texto de todos los nodos que cubre un rango.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## Ver también

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
