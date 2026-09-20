---
title: "Aspose::Words::Document::get_AttachedTemplate método"
linktitle: "get_AttachedTemplate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Document::get_AttachedTemplate método. Obtiene o establece la ruta completa de la plantilla adjunta al documento en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words/document/get_attachedtemplate/
---
## Document::get_AttachedTemplate method


Obtiene o establece la ruta completa de la plantilla adjunta al documento.

```cpp
System::String Aspose::Words::Document::get_AttachedTemplate()
```

## Observaciones


Una cadena vacía significa que el documento está adjunto a la plantilla Normal.

## Ejemplos



Muestra cómo establecer una plantilla predeterminada para documentos que no tienen plantillas adjuntas.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Habilita la actualización automática de estilos, pero no adjuntes un documento de plantilla.
doc->set_AutomaticallyUpdateStyles(true);

ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Dado que no hay un documento de plantilla, el documento no tenía dónde rastrear los cambios de estilo.
// Utilice un objeto SaveOptions para establecer automáticamente una plantilla
// si un documento que estamos guardando no tiene una.
System::SharedPtr<Aspose::Words::Saving::SaveOptions> options = Aspose::Words::Saving::SaveOptions::CreateSaveOptions(u"Document.DefaultTemplate.docx");
options->set_DefaultTemplate(get_MyDir() + u"Business brochure.dotx");

doc->Save(get_ArtifactsDir() + u"Document.DefaultTemplate.docx", options);
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
