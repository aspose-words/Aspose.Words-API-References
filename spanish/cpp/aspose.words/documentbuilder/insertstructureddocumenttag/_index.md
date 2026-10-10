---
title: "Método Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag"
linktitle: "InsertStructuredDocumentTag"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag. Inserta un StructuredDocumentTag en el documento en C++."
type: docs
weight: 46500
url: /es/cpp/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder::InsertStructuredDocumentTag method


Inserta un [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) en el documento.

```cpp
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> Aspose::Words::DocumentBuilder::InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType type)
```


### ReturnValue

El nodo [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) que acaba de insertarse.

## Ejemplos



Muestra cómo insertar simplemente una etiqueta de documento estructurado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveTo(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(3));
// Nota, que solo se permiten los siguientes tipos de StructuredDocumentTag para inserción:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// El nivel de marcado del StructuredDocumentTag insertado se detectará automáticamente y depende de la posición en la que se inserte.
// El StructuredDocumentTag añadido heredará el formato de párrafo y fuente desde la posición del cursor.
System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> sdtPlain = builder->InsertStructuredDocumentTag(Aspose::Words::Markup::SdtType::PlainText);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

## Ver también

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Enum [SdtType](../../../aspose.words.markup/sdttype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
