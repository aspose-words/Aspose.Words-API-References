---
title: "Método Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase"
linktitle: "get_HyperlinkBase"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase. Especifica la cadena base utilizada para evaluar hipervínculos relativos en este documento en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_hyperlinkbase/
---
## BuiltInDocumentProperties::get_HyperlinkBase method


Especifica la cadena base utilizada para evaluar los hipervínculos relativos en este documento.

```cpp
System::String Aspose::Words::Properties::BuiltInDocumentProperties::get_HyperlinkBase()
```

## Observaciones


Aspose.Words no utiliza esta propiedad.

## Ejemplos



Muestra cómo almacenar la parte base de un hipervínculo en las propiedades del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta un hipervínculo relativo a un documento en el sistema de archivos local llamado "Document.docx".
// Al hacer clic en el enlace en Microsoft Word se abrirá el documento designado, si está disponible.
builder->InsertHyperlink(u"Relative hyperlink", u"Document.docx", false);

// Este enlace es relativo. Si no hay "Document.docx" en la misma carpeta
// que el documento que contiene este enlace, el enlace quedará roto.
ASSERT_FALSE(System::IO::File::Exists(get_ArtifactsDir() + u"Document.docx"));
doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.BrokenLink.docx");

// El documento al que intentamos enlazar está en un directorio diferente al en el que planeamos guardar el documento.
// Podríamos corregir enlaces como este colocando un nombre de archivo absoluto en cada uno.
// Alternativamente, podríamos proporcionar un enlace base que cada hipervínculo con un nombre de archivo relativo
// se antepondrá a su enlace cuando hagamos clic en él.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();
properties->set_HyperlinkBase(get_MyDir());

ASSERT_TRUE(System::IO::File::Exists(properties->get_HyperlinkBase() + (System::ExplicitCast<Aspose::Words::Fields::FieldHyperlink>(doc->get_Range()->get_Fields()->idx_get(0)))->get_Address()));

doc->Save(get_ArtifactsDir() + u"DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

## Ver también

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
