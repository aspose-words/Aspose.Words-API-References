---
title: "Aspose::Words::Font::get_BoldBi método"
linktitle: "get_BoldBi"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_BoldBi método. Verdadero si el texto de derecha a izquierda está formateado en negrita en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/font/get_boldbi/
---
## Font::get_BoldBi method


Verdadero si el texto de derecha a izquierda está formateado en negrita.

```cpp
bool Aspose::Words::Font::get_BoldBi()
```


## Ejemplos



Muestra cómo definir conjuntos separados de configuraciones de fuente para texto de derecha a izquierda y texto de derecha a izquierda.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Defina un conjunto de configuraciones de fuente para texto de izquierda a derecha.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Defina otro conjunto de configuraciones de fuente para texto de derecha a izquierda.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// También podemos usar la bandera Bidi para indicar si el texto que estamos a punto de agregar
// con el document builder es de derecha a izquierda. Cuando agregamos texto con esta bandera establecida en verdadero,
// se formateará usando el conjunto de configuraciones de fuente de derecha a izquierda.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// Establezca la bandera en falso y luego agregue texto de izquierda a derecha.
// El document builder formateará estos usando el conjunto de configuraciones de fuente de izquierda a derecha.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## Ver también

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
