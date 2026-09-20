---
title: "Clase Aspose::Words::Fields::FieldCollection"
linktitle: "FieldCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Fields::FieldCollection. Una colección de objetos Field que representa los campos en el rango especificado. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 23000
url: /es/cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


Una colección de objetos [Field](../field/) que representa los campos en el rango especificado. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Clear](./clear/)() | Elimina todos los campos de esta colección del documento y de la propia colección. |
| [get_Count](./get_count/)() | Devuelve el número de campos en la colección. |
| [GetEnumerator](./getenumerator/)() override | Devuelve un objeto enumerador. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Devuelve un campo en el índice especificado. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | Elimina el campo especificado de esta colección y del documento. |
| [RemoveAt](./removeat/)(int32_t) | Elimina un campo en el índice especificado de esta colección y del documento. |
| static [Type](./type/)() |  |
## Observaciones


Una instancia de esta colección itera los campos que comienzan dentro del rango especificado.

La colección [FieldCollection](./) no posee los campos que contiene, sino que es solo una selección de campos.

La colección [FieldCollection](./) es "en vivo", es decir, los cambios en los hijos del objeto nodo del que se creó se reflejan inmediatamente en los campos devueltos por las propiedades y métodos de [FieldCollection](./).

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
