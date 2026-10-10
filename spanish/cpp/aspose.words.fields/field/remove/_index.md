---
title: "Método Aspose::Words::Fields::Field::Remove"
linktitle: "Remove"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Fields::Field::Remove. Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve null en C++."
type: docs
weight: 17000
url: /es/cpp/aspose.words.fields/field/remove/
---
## Field::Remove method


Elimina el campo del documento. Devuelve un nodo justo después del campo. Si el final del campo es el último hijo de su nodo padre, devuelve su párrafo padre. Si el campo ya está eliminado, devuelve **null**.

```cpp
virtual System::SharedPtr<Aspose::Words::Node> Aspose::Words::Fields::Field::Remove()
```


## Ejemplos



Muestra cómo eliminar campos de una colección de campos.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// A continuación se presentan cuatro formas de eliminar campos de una colección de campos.
// 1 -  Obtén un campo para que se elimine a sí mismo:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Obtén la colección para eliminar un campo que pasamos a su método de eliminación:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Elimina un campo de una colección en un índice:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Elimina todos los campos de la colección de una vez:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## Ver también

* Class [Node](../../../aspose.words/node/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
