---
title: "Método Aspose::Words::Font::get_ComplexScript"
linktitle: "get_ComplexScript"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Font::get_ComplexScript. Especifica si el contenido de esta ejecución debe tratarse como texto de script complejo independientemente de sus valores de caracteres Unicode al determinar el formato de esta ejecución en C++."
type: docs
weight: 10000
url: /es/cpp/aspose.words/font/get_complexscript/
---
## Font::get_ComplexScript method


Especifica si el contenido de esta ejecución debe tratarse como texto de escritura compleja sin importar sus valores de caracteres Unicode al determinar el formato de esta ejecución.

```cpp
bool Aspose::Words::Font::get_ComplexScript()
```


## Ejemplos



Muestra cómo agregar texto que siempre se trata como script complejo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_ComplexScript(true);

builder->Writeln(u"Text treated as complex script.");

doc->Save(get_ArtifactsDir() + u"Font.ComplexScript.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
