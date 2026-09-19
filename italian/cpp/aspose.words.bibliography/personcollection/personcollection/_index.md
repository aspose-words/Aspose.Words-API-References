---
title: "Aspose::Words::Bibliography::PersonCollection::PersonCollection costruttore"
linktitle: "PersonCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Bibliography::PersonCollection::PersonCollection costruttore. Inizializza una nuova istanza della classe PersonCollection in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection::PersonCollection() constructor


Inizializza una nuova istanza della classe [PersonCollection](../).

```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection()
```


## Esempi



Mostra come lavorare con la collezione di persone.
```cpp
// Crea una nuova collezione di persone.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Aggiungi una nuova persona alla collezione.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Rimuovi la persona dalla collezione se esiste.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Crea una collezione di persone con due persone.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Rimuovi la persona dalla collezione per indice.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Rimuovi tutte le persone dalla collezione.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Vedi anche

* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
## PersonCollection::PersonCollection(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\&) constructor


Inizializza una nuova istanza della classe [PersonCollection](../).

```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Bibliography::Person>> &persons)
```


## Esempi



Mostra come lavorare con la collezione di persone.
```cpp
// Crea una nuova collezione di persone.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Aggiungi una nuova persona alla collezione.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Rimuovi la persona dalla collezione se esiste.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Crea una collezione di persone con due persone.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Rimuovi la persona dalla collezione per indice.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Rimuovi tutte le persone dalla collezione.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Vedi anche

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
## PersonCollection::PersonCollection(const System::SharedPtr\<System::Collections::Generic::IEnumerable\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\>\&) constructor




```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection(const System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Person>>> &persons)
```

## Vedi anche

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
