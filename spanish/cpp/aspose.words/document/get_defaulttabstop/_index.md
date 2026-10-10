---
title: "Aspose::Words::Document::get_DefaultTabStop método"
linktitle: "get_DefaultTabStop"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_DefaultTabStop método. Obtiene o establece el intervalo (en puntos) entre los tabuladores predeterminados en C++."
type: docs
weight: 20000
url: /es/cpp/aspose.words/document/get_defaulttabstop/
---
## Document::get_DefaultTabStop method


Obtiene o establece el intervalo (en puntos) entre los tabuladores predeterminados.

```cpp
double Aspose::Words::Document::get_DefaultTabStop()
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

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
