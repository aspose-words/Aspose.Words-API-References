---
title: "Aspose::Words::Font::get_Italic método"
linktitle: "get_Italic"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_Italic. Verdadero si la fuente está formateada en cursiva en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


True si la fuente está formateada en cursiva.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## Ejemplos



Muestra cómo escribir texto en cursiva usando un DocumentBuilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
