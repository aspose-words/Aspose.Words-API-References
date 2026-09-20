---
title: "Método Aspose::Words::Bibliography::PersonCollection::Add"
linktitle: "Add"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Bibliography::PersonCollection::Add. Añade una Persona a la colección en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.bibliography/personcollection/add/
---
## PersonCollection::Add method


Añade una [Person](../../person/) a la colección.

```cpp
void Aspose::Words::Bibliography::PersonCollection::Add(const System::SharedPtr<Aspose::Words::Bibliography::Person> &person)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| persona | const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\& | La persona a añadir a la colección. |

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

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
