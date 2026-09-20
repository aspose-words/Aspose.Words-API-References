---
title: "Aspose::Words::Font::get_NameOther método"
linktitle: "get_NameOther"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_NameOther método. Devuelve o establece la fuente utilizada para los caracteres con códigos de carácter de 128 a 255 en C++."
type: docs
weight: 29000
url: /es/cpp/aspose.words/font/get_nameother/
---
## Font::get_NameOther method


Devuelve o establece la fuente utilizada para los caracteres con códigos de carácter de 128 a 255.

```cpp
System::String Aspose::Words::Font::get_NameOther()
```


## Ejemplos



Muestra cómo Microsoft Word puede combinar dos fuentes diferentes en una misma ejecución.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Supongamos una ejecución que usamos el generador para insertar mientras utilizamos esta configuración de fuente
// contiene caracteres dentro del rango de caracteres ASCII. En ese caso,
// mostrará esos caracteres usando esta fuente.
builder->get_Font()->set_NameAscii(u"Calibri");

// Sin especificar otra fuente, el generador también aplicará esta fuente a todos los caracteres que inserte.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// Especifique una fuente para usar con todos los caracteres fuera del rango ASCII.
// Idealmente, esta fuente debería tener un glifo para cada código de carácter no ASCII requerido.
builder->get_Font()->set_NameOther(u"Courier New");

// Inserte una ejecución con una palabra compuesta de caracteres ASCII, y una palabra con todos los caracteres fuera de ese rango.
// Cada carácter se mostrará usando una de las fuentes, dependiendo de.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
