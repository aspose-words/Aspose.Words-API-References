---
title: "Método Aspose::Words::Section::get_ProtectedForForms"
linktitle: "get_ProtectedForForms"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Section::get_ProtectedForForms. Verdadero si la sección está protegida para formularios. Cuando una sección está protegida para formularios, los usuarios pueden seleccionar y modificar texto solo en los campos de formulario en Microsoft Word en C++."
type: docs
weight: 14000
url: /es/cpp/aspose.words/section/get_protectedforforms/
---
## Section::get_ProtectedForForms method


Verdadero si la sección está protegida para formularios. Cuando una sección está protegida para formularios, los usuarios pueden seleccionar y modificar texto solo en los campos de formulario en Microsoft Word.

```cpp
bool Aspose::Words::Section::get_ProtectedForForms()
```


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

* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
