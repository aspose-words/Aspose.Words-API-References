---
title: "Aspose::Words::Fields::TextFormFieldType enumeración"
linktitle: "TextFormFieldType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::TextFormFieldType enumeración. Especifica el tipo de un campo de formulario de texto en C++."
type: docs
weight: 134000
url: /es/cpp/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enum


Especifica el tipo de un campo de formulario de texto.

```cpp
enum class TextFormFieldType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Regular | 0 | El campo de formulario de texto puede contener cualquier texto. |
| Number | 1 | El campo de formulario de texto solo puede contener números. |
| Fecha | 2 | El campo de formulario de texto solo puede contener un valor de fecha válido. |
| CurrentDate | 3 | El valor del campo de formulario de texto es la fecha actual cuando se actualiza el campo. |
| CurrentTime | 4 | El valor del campo de formulario de texto es la hora actual cuando se actualiza el campo. |
| Calculated | 5 | El valor del campo de formulario de texto se calcula a partir de la expresión especificada en la propiedad [TextInputDefault](../formfield/get_textinputdefault/). |


## Ejemplos



Muestra cómo crear campos de formulario.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// Los campos de formulario son objetos en el documento con los que el usuario puede interactuar al ser solicitado a ingresar valores.
// Podemos crearlos usando un generador de documentos, y a continuación se presentan dos formas de hacerlo.
// 1 -  Entrada de texto básica:
builder->InsertTextInput(u"My text input", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your name here", 30);

// 2 -  Cuadro combinado con texto de indicación y un rango de valores posibles:
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"-- Select your favorite footwear --", u"Sneakers", u"Oxfords", u"Flip-flops", u"Other"});

builder->InsertParagraph();
builder->InsertComboBox(u"My combo box", items, 0);

builder->get_Document()->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateForm.docx");
```

## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
