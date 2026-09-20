---
title: "Aspose::Words::DocumentBuilder::MoveToField método"
linktitle: "MoveToField"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::MoveToField método. Mueve el cursor a un campo en el documento en C++."
type: docs
weight: 56000
url: /es/cpp/aspose.words/documentbuilder/movetofield/
---
## DocumentBuilder::MoveToField method


Mueve el cursor a un campo en el documento.

```cpp
void Aspose::Words::DocumentBuilder::MoveToField(const System::SharedPtr<Aspose::Words::Fields::Field> &field, bool isAfter)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| campo | const System::SharedPtr\<Aspose::Words::Fields::Field\>\& | El campo al que mover el cursor. |
| isAfter | bool | Cuando **true**, mueve el cursor para que quede después del final del campo. Cuando **false**, mueve el cursor para que quede antes del inicio del campo. |

## Ejemplos



Muestra cómo mover el cursor del punto de inserción de nodos de un document builder a un campo específico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte un campo usando el DocumentBuilder y añada una secuencia de texto después de él.
System::SharedPtr<Aspose::Words::Fields::Field> field = builder->InsertField(u" AUTHOR \"John Doe\" ");

// El cursor del builder está actualmente al final del documento.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Mueva el cursor al campo especificando si colocar ese cursor antes o después del campo.
builder->MoveToField(field, moveCursorToAfterTheField);

// Observe que el cursor está fuera del campo en ambos casos.
// Esto significa que no podemos editar el campo usando el builder de esta manera.
// Para editar un campo, podemos usar el método MoveTo del builder sobre el FieldStart de un campo.
// o el nodo FieldSeparator para colocar el cursor dentro.
if (moveCursorToAfterTheField)
{
    ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));
    builder->Write(u" Text immediately after the field.");

    ASSERT_EQ(u"\u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015 Text immediately after the field.", doc->GetText().Trim());
}
else
{
    ASPOSE_ASSERT_EQ(field->get_Start(), builder->get_CurrentNode());
    builder->Write(u"Text immediately before the field. ");

    ASSERT_EQ(u"Text immediately before the field. \u0013 AUTHOR \"John Doe\" \u0014John Doe\u0015", doc->GetText().Trim());
}
```

## Ver también

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
