---
title: "Método Aspose::Words::Document::get_AutomaticallyUpdateStyles"
linktitle: "get_AutomaticallyUpdateStyles"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_AutomaticallyUpdateStyles. Obtiene o establece una bandera que indica si los estilos del documento se actualizan para coincidir con los estilos de la plantilla adjunta cada vez que el documento se abre en MS Word en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words/document/get_automaticallyupdatestyles/
---
## Document::get_AutomaticallyUpdateStyles method


Obtiene o establece una bandera que indica si los estilos del documento se actualizan para coincidir con los estilos de la plantilla adjunta cada vez que el documento se abre en MS Word.

```cpp
bool Aspose::Words::Document::get_AutomaticallyUpdateStyles()
```


## Ejemplos



Muestra cómo adjuntar una plantilla a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Los documentos de Microsoft Word, por defecto, vienen con una plantilla adjunta llamada "Normal.dotm".
// No hay una plantilla predeterminada para documentos en blanco de Aspose.Words.
ASSERT_EQ(System::String::Empty, doc->get_AttachedTemplate());

// Adjunte una plantilla, luego establezca la bandera para aplicar cambios de estilo
// dentro de la plantilla a los estilos de nuestro documento.
doc->set_AttachedTemplate(get_MyDir() + u"Business brochure.dotx");
doc->set_AutomaticallyUpdateStyles(true);

doc->Save(get_ArtifactsDir() + u"Document.AutomaticallyUpdateStyles.docx");
```


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
