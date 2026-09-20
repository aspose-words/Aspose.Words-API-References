---
title: "Método Aspose::Words::Fields::FieldOptions::get_PreProcessCulture"
linktitle: "get_PreProcessCulture"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FieldOptions::get_PreProcessCulture. Obtiene o establece la cultura para preprocesar los valores de los campos en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.fields/fieldoptions/get_preprocessculture/
---
## FieldOptions::get_PreProcessCulture method


Obtiene o establece la cultura para preprocesar los valores de los campos.

```cpp
const System::SharedPtr<System::Globalization::CultureInfo> & Aspose::Words::Fields::FieldOptions::get_PreProcessCulture() const
```

## Observaciones


Actualmente esta propiedad solo afecta el valor del campo [FieldDocProperty](../../fielddocproperty/).

El valor predeterminado es **null**. Cuando esta propiedad se establece en **null**, el valor del campo [FieldDocProperty](../../fielddocproperty/) se preprocesa con la cultura controlada por la propiedad [FieldUpdateCultureSource](../get_fieldupdateculturesource/).

## Ejemplos



Muestra cómo establecer la cultura de preprocesamiento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Establezca la cultura según la cual algunos campos formatearán sus valores mostrados.
doc->get_FieldOptions()->set_PreProcessCulture(System::MakeObject<System::Globalization::CultureInfo>(u"de-DE"));

System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" DOCPROPERTY CreateTime");

// El campo DOCPROPERTY mostrará su resultado formateado según la cultura de preprocesamiento
// que hemos configurado a alemán. El campo mostrará la fecha/hora usando el formato "dd.mm.yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[.]\\d{2}[.]\\d{4} \\d{2}[:]\\d{2}")->get_Success());

doc->get_FieldOptions()->set_PreProcessCulture(System::Globalization::CultureInfo::get_InvariantCulture());
field->Update();

// Después de cambiar a la cultura invariante, el campo DOCPROPERTY usará el formato "mm/dd/yyyy hh:mm".
ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(field->get_Result(), u"\\d{2}[/]\\d{2}[/]\\d{4} \\d{2}[:]\\d{2}")->get_Success());
```

## Ver también

* Class [FieldOptions](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
