---
title: "Aspose::Words::DocumentBuilder::InsertComboBox method"
linktitle: "InsertComboBox"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertComboBox method. Inserta un campo de formulario combobox en la posición actual en C++."
type: docs
weight: 32000
url: /es/cpp/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder::InsertComboBox method


Inserta un campo de formulario de cuadro combinado en la posición actual.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertComboBox(const System::String &name, const System::ArrayPtr<System::String> &items, int32_t selectedIndex)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del campo de formulario. Puede ser una cadena vacía. El valor con más de 20 caracteres será truncado. |
| items | const System::ArrayPtr\<System::String\>\& | Los elementos del ComboBox. El máximo es 25 elementos. |
| selectedIndex | int32_t | El índice del elemento seleccionado en el ComboBox. |

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


Muestra cómo insertar un campo de formulario combo box en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserta un formulario que solicita al usuario seleccionar uno de los elementos del menú.
builder->Write(u"Pick a fruit: ");
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"});
builder->InsertComboBox(u"DropDown", items, 0);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertComboBox.docx");
```

## Ver también

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
