---
title: "Aspose::Words::Font::get_Hidden método"
linktitle: "get_Hidden"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_Hidden método. Verdadero si la fuente está formateada como texto oculto en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


Verdadero si la fuente está formateada como texto oculto.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## Ejemplos



Muestra cómo crear una secuencia de texto oculto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Con la bandera Hidden establecida en verdadero, cualquier texto que creemos usando este objeto Font será invisible en el documento.
// No veremos ni resaltaremos texto oculto a menos que activemos la opción "Hidden text"
// se encuentra en Microsoft Word a través de "File" -> "Options" -> "Display". El texto seguirá allí,
// y podremos acceder a este texto programáticamente.
// No se recomienda usar este método para ocultar información sensible.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
