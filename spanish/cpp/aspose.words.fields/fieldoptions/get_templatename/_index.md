---
title: "Aspose::Words::Fields::FieldOptions::get_TemplateName método"
linktitle: "get_TemplateName"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldOptions::get_TemplateName método. Obtiene o establece el nombre de archivo de la plantilla utilizada por el documento en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.fields/fieldoptions/get_templatename/
---
## FieldOptions::get_TemplateName method


Obtiene o establece el nombre de archivo de la plantilla utilizada por el documento.

```cpp
System::String Aspose::Words::Fields::FieldOptions::get_TemplateName() const
```

## Observaciones


Esta propiedad es utilizada por el campo [FieldTemplate](../../fieldtemplate/) si la propiedad [AttachedTemplate](../../../aspose.words/document/get_attachedtemplate/) está vacía.

Si esta propiedad está vacía, se utiliza el nombre de archivo de plantilla predeterminado **Normal.dotm**.

## Ejemplos



Muestra cómo usar un campo TEMPLATE para mostrar la ubicación en el sistema de archivos local de la plantilla de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Podemos establecer un nombre de plantilla mediante los campos. Esta propiedad se usa cuando "doc.AttachedTemplate" está vacío.
// Si esta propiedad está vacía, se utiliza el nombre de archivo de plantilla predeterminado "Normal.dotm".
doc->get_FieldOptions()->set_TemplateName(System::String::Empty);

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
ASSERT_EQ(u" TEMPLATE ", field->GetFieldCode());

builder->Writeln();
field = System::ExplicitCast<Aspose::Words::Fields::FieldTemplate>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTemplate, false));
field->set_IncludeFullPath(true);

ASSERT_EQ(u" TEMPLATE  \\p", field->GetFieldCode());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.TEMPLATE.docx");
```

## Ver también

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
