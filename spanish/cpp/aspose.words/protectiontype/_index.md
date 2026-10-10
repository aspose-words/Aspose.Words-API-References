---
title: "Aspose::Words::ProtectionType enumeración"
linktitle: "ProtectionType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ProtectionType enumeración. Tipo de protección para un documento en C++."
type: docs
weight: 111000
url: /es/cpp/aspose.words/protectiontype/
---
## ProtectionType enum


Tipo de protección para un documento.

```cpp
enum class ProtectionType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AllowOnlyComments | 1 | El usuario solo puede modificar los comentarios en el documento. |
| AllowOnlyFormFields | 2 | El usuario solo puede introducir datos en los campos de formulario del documento. |
| AllowOnlyRevisions | 0 | El usuario solo puede añadir marcas de revisión al documento. |
| ReadOnly | 3 | No se permiten cambios en el documento. Disponible desde Microsoft Word 2003. |
| NoProtection | -1 | El documento no está protegido. |


## Ejemplos



Muestra cómo desactivar la protección para una sección.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Section 1. Hello world!");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

builder->Writeln(u"Section 2. Hello again!");
builder->Write(u"Please enter text here: ");
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// Aplicar protección de escritura a cada sección del documento.
doc->Protect(Aspose::Words::ProtectionType::AllowOnlyFormFields);

// Desactivar la protección de escritura para la primera sección.
doc->get_Sections()->idx_get(0)->set_ProtectedForForms(false);

// En este documento de salida, podremos editar la primera sección libremente,
// y solo podremos editar el contenido del campo de formulario en la segunda sección.
doc->Save(get_ArtifactsDir() + u"Section.Protect.docx");
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
