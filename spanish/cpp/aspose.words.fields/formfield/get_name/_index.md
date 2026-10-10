---
title: "Método Aspose::Words::Fields::FormField::get_Name"
linktitle: "get_Name"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::FormField::get_Name. Obtiene o establece el nombre del campo de formulario en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.fields/formfield/get_name/
---
## FormField::get_Name method


Obtiene o establece el nombre del campo de formulario.

```cpp
System::String Aspose::Words::Fields::FormField::get_Name()
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

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
