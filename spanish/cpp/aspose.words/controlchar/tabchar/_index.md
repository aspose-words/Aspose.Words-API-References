---
title: "Aspose::Words::ControlChar::TabChar campo"
linktitle: "TabChar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ControlChar::TabChar campo. Carácter de tabulación: (char)9 o \"\\t\" en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words/controlchar/tabchar/
---
## TabChar field


Carácter de tabulación: (char)9 o "\t".

```cpp
static constexpr char16_t Aspose::Words::ControlChar::TabChar
```


## Ejemplos



Muestra cómo establecer un intervalo personalizado para las posiciones de los tabuladores.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establezca los tabuladores para que aparezcan cada 72 puntos (1 pulgada).
builder->get_Document()->set_DefaultTabStop(72);

// Cada carácter de tabulación ajusta el texto posterior a la posición del tabulador más cercana.
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::Tab() + u"World!");
builder->Writeln(System::String(u"Hello") + Aspose::Words::ControlChar::TabChar + u"World!");
```

## Ver también

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
