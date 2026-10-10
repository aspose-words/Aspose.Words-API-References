---
title: "Aspose::Words::DocumentBuilder::InsertCheckBox method"
linktitle: "InsertCheckBox"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertCheckBox method. Inserta un campo de formulario de casilla de verificación en la posición actual en C++."
type: docs
weight: 31000
url: /es/cpp/aspose.words/documentbuilder/insertcheckbox/
---
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, int32_t) method


Inserta un campo de formulario de casilla de verificación en la posición actual.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool checkedValue, int32_t size)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del campo de formulario. Puede ser una cadena vacía. El valor con más de 20 caracteres será truncado. |
| checkedValue | bool | Estado marcado del campo de formulario de casilla de verificación. |
| size | int32_t | Especifica el tamaño de la casilla de verificación en puntos. Especifique 0 para que MS Word calcule automáticamente el tamaño de la casilla de verificación. |

### ReturnValue

El nodo del campo de formulario que se acaba de insertar.
## Observaciones


Si especificas un nombre para el campo de formulario, se crea automáticamente un marcador con el mismo nombre.

## Ejemplos



Muestra cómo insertar casillas de verificación en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte casillas de verificación de tamaños variados y estados marcados predeterminados.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Los campos de formulario tienen un límite de longitud de nombre de 20 caracteres.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Podemos interactuar con estas casillas de verificación en Microsoft Word haciendo doble clic sobre ellas.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Ver también

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertCheckBox(const System::String\&, bool, bool, int32_t) method


Inserta un campo de formulario de casilla de verificación en la posición actual.

```cpp
System::SharedPtr<Aspose::Words::Fields::FormField> Aspose::Words::DocumentBuilder::InsertCheckBox(const System::String &name, bool defaultValue, bool checkedValue, int32_t size)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| name | const System::String\& | El nombre del campo de formulario. Puede ser una cadena vacía. El valor con más de 20 caracteres será truncado. |
| defaultValue | bool | Valor predeterminado del campo de formulario de casilla de verificación. |
| checkedValue | bool | Estado actual marcado del campo de formulario de casilla de verificación. |
| size | int32_t | Especifica el tamaño de la casilla de verificación en puntos. Especifique 0 para que MS Word calcule automáticamente el tamaño de la casilla de verificación. |

### ReturnValue

El nodo del campo de formulario que se acaba de insertar.
## Observaciones


Si especificas un nombre para el campo de formulario, se crea automáticamente un marcador con el mismo nombre.

## Ejemplos



Muestra cómo insertar casillas de verificación en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte casillas de verificación de tamaños variados y estados marcados predeterminados.
builder->Write(u"Unchecked check box of a default size: ");
builder->InsertCheckBox(System::String::Empty, false, false, 0);
builder->InsertParagraph();

builder->Write(u"Large checked check box: ");
builder->InsertCheckBox(u"CheckBox_Default", true, true, 50);
builder->InsertParagraph();

// Los campos de formulario tienen un límite de longitud de nombre de 20 caracteres.
builder->Write(u"Very large checked check box: ");
builder->InsertCheckBox(u"CheckBox_OnlyCheckedValue", true, 100);

ASSERT_EQ(u"CheckBox_OnlyChecked", doc->get_Range()->get_FormFields()->idx_get(2)->get_Name());

// Podemos interactuar con estas casillas de verificación en Microsoft Word haciendo doble clic sobre ellas.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertCheckBox.docx");
```

## Ver también

* Class [FormField](../../../aspose.words.fields/formfield/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
