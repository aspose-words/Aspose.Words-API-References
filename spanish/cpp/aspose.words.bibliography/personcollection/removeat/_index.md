---
title: "Aspose::Words::Bibliography::PersonCollection::RemoveAt method"
linktitle: "RemoveAt"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Bibliography::PersonCollection::RemoveAt method. Elimina la persona en el índice especificado en C++."
type: docs
weight: 12000
url: /es/cpp/aspose.words.bibliography/personcollection/removeat/
---
## PersonCollection::RemoveAt method


Elimina a la persona en el índice especificado.

```cpp
void Aspose::Words::Bibliography::PersonCollection::RemoveAt(int32_t index)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| index | int32_t | El índice basado en cero de la persona a eliminar. |

## Ejemplos



Muestra cómo trabajar con la colección de personas.
```cpp
// Crea una nueva colección de personas.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Añade una nueva persona a la colección.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Elimina la persona de la colección si existe.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Crea una colección de personas con dos personas.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Eliminar persona de la colección por el índice.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Eliminar todas las personas de la colección.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Ver también

* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
