---
title: "Aspose::Words::DocumentBuilder::InsertTextInput method"
linktitle: "InsertTextInput"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertTextInput method. Inserta un campo de formulario de texto en la posición actual en C++."
type: docs
weight: 49000
url: /es/cpp/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder::InsertTextInput method


Inserta un campo de formulario de texto en la posición actual.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertTextInput(const System::String &name, Aspose::Words::Fields::TextFormFieldType type, const System::String &format, const System::String &fieldValue, int32_t maxLength)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del campo de formulario. Puede ser una cadena vacía. |
| tipo | Aspose::Words::Fields::TextFormFieldType | Especifica el tipo del campo de formulario de texto. |
| formato | const System::String\& | Cadena de formato utilizada para formatear el valor del campo de formulario. |
| fieldValue | const System::String\& | Texto que se mostrará en el campo. |
| maxLength | int32_t | Longitud máxima que el usuario puede ingresar en el campo de formulario. Establezca a cero para longitud ilimitada. |

### ReturnValue

El nodo del campo de formulario que se acaba de insertar.
## Observaciones


Si especificas un nombre para el campo de formulario, se crea automáticamente un marcador con el mismo nombre.

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


Muestra cómo insertar un campo de formulario de entrada de texto en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un formulario que solicite al usuario ingresar texto.
builder->InsertTextInput(u"TextInput", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Enter your text here", 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTextInput.docx");
```


Muestra cómo insertar un campo de formulario de entrada de texto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please enter text here: ");

// Inserte un campo de entrada de texto, que permitirá al usuario hacer clic en él e ingresar texto.
// Asigne un texto de marcador de posición que el usuario pueda sobrescribir y pasar.
// una longitud máxima de texto de 0 para no aplicar límite al contenido del campo del formulario.
builder->InsertTextInput(u"TextInput1", Aspose::Words::Fields::TextFormFieldType::Regular, u"", u"Placeholder text", 0);

// El campo del formulario aparecerá como una etiqueta "input" html, con un tipo "text".
doc->Save(get_ArtifactsDir() + u"FormFields.TextInput.html");
```

## Ver también

* Class [FormField](../../../aspose.words.fields/formfield/)
* Enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
