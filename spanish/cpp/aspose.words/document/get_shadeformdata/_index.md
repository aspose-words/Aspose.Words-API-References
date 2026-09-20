---
title: "Aspose::Words::Document::get_ShadeFormData method"
linktitle: "get_ShadeFormData"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_ShadeFormData method. Especifica si se debe activar el sombreado gris en los campos de formulario en C++."
type: docs
weight: 49000
url: /es/cpp/aspose.words/document/get_shadeformdata/
---
## Document::get_ShadeFormData method


Especifica si se activa el sombreado gris en los campos de formulario.

```cpp
bool Aspose::Words::Document::get_ShadeFormData()
```


## Ejemplos



Muestra cómo aplicar sombreado gris a los campos de formulario.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world! ");
builder->InsertTextInput(u"My form field", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Text contents of form field, which are shaded in grey by default.", 0);

// Podemos desactivar el sombreado gris, de modo que el texto marcado se mezcle con el resto del texto.
doc->set_ShadeFormData(useGreyShading);
doc->Save(get_ArtifactsDir() + u"Document.ShadeFormData.docx");
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
