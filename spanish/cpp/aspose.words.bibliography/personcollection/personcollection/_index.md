---
title: "Aspose::Words::Bibliography::PersonCollection::PersonCollection constructor"
linktitle: "PersonCollection"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Bibliography::PersonCollection::PersonCollection constructor. Inicializa una nueva instancia de la clase PersonCollection en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection::PersonCollection() constructor


Inicializa una nueva instancia de la clase [PersonCollection](../).

```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection()
```


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
## PersonCollection::PersonCollection(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\&) constructor


Inicializa una nueva instancia de la clase [PersonCollection](../).

```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Bibliography::Person>> &persons)
```


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
## PersonCollection::PersonCollection(const System::SharedPtr\<System::Collections::Generic::IEnumerable\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\>\&) constructor




```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection(const System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Person>>> &persons)
```

## Ver también

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
