---
title: "Método Aspose::Words::Saving::SaveOptions::get_DefaultTemplate"
linktitle: "get_DefaultTemplate"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::SaveOptions::get_DefaultTemplate. Obtiene o establece la ruta a la plantilla predeterminada (incluyendo el nombre de archivo). El valor predeterminado para esta propiedad es una cadena vacía en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words.saving/saveoptions/get_defaulttemplate/
---
## SaveOptions::get_DefaultTemplate method


Obtiene o establece la ruta a la plantilla predeterminada (incluido el nombre de archivo). El valor predeterminado para esta propiedad es **empty string**.

```cpp
System::String Aspose::Words::Saving::SaveOptions::get_DefaultTemplate() const
```


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

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
