---
title: "Aspose::Words::Saving::SaveOptions::CreateSaveOptions método"
linktitle: "CreateSaveOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::SaveOptions::CreateSaveOptions. Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.saving/saveoptions/createsaveoptions/
---
## SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat) method


Crea un objeto de opciones de guardado de una clase adecuada para el formato de guardado especificado.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado para el cual crear un objeto de opciones de guardado. |

### ReturnValue

Un objeto de una clase que deriva de [SaveOptions](../).

## Ver también

* Class [SaveOptions](../)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## SaveOptions::CreateSaveOptions(const System::String\&) method


Crea un objeto de opciones de guardado de una clase adecuada para la extensión de archivo especificada en el nombre de archivo proporcionado.

```cpp
static System::SharedPtr<Aspose::Words::Saving::SaveOptions> Aspose::Words::Saving::SaveOptions::CreateSaveOptions(const System::String &fileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | La extensión de este nombre de archivo determina la clase del objeto de opciones de guardado a crear. |

### ReturnValue

Un objeto de una clase que deriva de [SaveOptions](../).

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
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
