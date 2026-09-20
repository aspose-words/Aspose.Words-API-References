---
title: "Método Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath"
linktitle: "get_IncludeFullPath"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath. Obtiene o establece si se debe incluir el nombre completo de la ruta del archivo en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.fields/fieldtemplate/get_includefullpath/
---
## FieldTemplate::get_IncludeFullPath method


Obtiene o establece si se debe incluir el nombre completo de la ruta del archivo.

```cpp
bool Aspose::Words::Fields::FieldTemplate::get_IncludeFullPath()
```


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

* Class [FieldTemplate](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
