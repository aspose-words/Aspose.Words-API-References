---
title: "Aspose::Words::Fields::FormField::get_Type método"
linktitle: "get_Type"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FormField::get_Type método. Devuelve el tipo de campo de formulario en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words.fields/formfield/get_type/
---
## FormField::get_Type method


Devuelve el tipo de campo de formulario.

```cpp
Aspose::Words::Fields::FieldType Aspose::Words::Fields::FormField::get_Type()
```


## Ejemplos



Muestra cómo insertar un cuadro combinado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Inserte un cuadro combinado que permitirá al usuario elegir una opción de una colección de cadenas.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// El campo de formulario aparecerá en forma de una etiqueta HTML "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```

## Ver también

* Enum [FieldType](../../fieldtype/)
* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
