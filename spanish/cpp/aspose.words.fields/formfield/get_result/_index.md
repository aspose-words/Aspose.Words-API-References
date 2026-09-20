---
title: "Aspose::Words::Fields::FormField::get_Result método"
linktitle: "get_Result"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FormField::get_Result método. Obtiene o establece una cadena que representa el resultado de este campo de formulario en C++."
type: docs
weight: 19000
url: /es/cpp/aspose.words.fields/formfield/get_result/
---
## FormField::get_Result method


Obtiene o establece una cadena que representa el resultado de este campo de formulario.

```cpp
System::String Aspose::Words::Fields::FormField::get_Result()
```

## Observaciones


Para un campo de formulario de texto, el resultado es el texto que está en el campo.

Para un campo de formulario de casilla de verificación, el resultado puede ser \"1\" o \"0\" para indicar marcado o desmarcado.

Para un campo de formulario desplegable, el resultado es la cadena seleccionada en el desplegable.

Establecer [Result](./) para un campo de formulario de texto no aplica el formato de texto especificado en [TextInputFormat](../get_textinputformat/). Si deseas establecer un valor y aplicar el formato, usa el método [SetTextInputValue()](../).

Para un campo de formulario de texto, el valor [TextInputDefault](../get_textinputdefault/) se aplica si *value* es **null**.

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
