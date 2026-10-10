---
title: "Aspose::Words::Font::get_Bidi método"
linktitle: "get_Bidi"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Font::get_Bidi método. Especifica si el contenido de esta ejecución debe tener características de derecha a izquierda en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/font/get_bidi/
---
## Font::get_Bidi method


Especifica si el contenido de esta ejecución debe tener características de derecha a izquierda.

```cpp
bool Aspose::Words::Font::get_Bidi()
```

## Observaciones


Esta propiedad, cuando está activada, no debe usarse con texto fuertemente de izquierda a derecha. Cualquier comportamiento bajo esa condición no está especificado. Esta propiedad, cuando está desactivada, no debe usarse con texto fuertemente de derecha a izquierda. Cualquier comportamiento bajo esa condición no está especificado.

Cuando se muestra el contenido de esta ejecución, todos los caracteres deben tratarse como caracteres de escritura compleja para fines de formato. Esto significa que [BoldBi](../get_boldbi/), [ItalicBi](../get_italicbi/), [SizeBi](../get_sizebi/) y un nombre de fuente correspondiente se utilizarán al renderizar esta ejecución.

Además, cuando se muestra el contenido de esta ejecución, esta propiedad actúa como una sobrescritura de derecha a izquierda para los caracteres que se clasifican como "tipos débiles" y "tipos neutrales".

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
