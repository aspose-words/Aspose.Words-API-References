---
title: "Aspose::Words::Bibliography::PersonCollection::PersonCollection konstruktor"
linktitle: "PersonCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Bibliography::PersonCollection::PersonCollection konstruktor. Initierar en ny instans av PersonCollection-klassen i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.bibliography/personcollection/personcollection/
---
## PersonCollection::PersonCollection() constructor


Initiera en ny instans av klassen [PersonCollection](../).

```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection()
```


## Exempel



Visar hur man arbetar med personsamlingen.
```cpp
// Skapa en ny personsamling.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Lägg till en ny person i samlingen.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Ta bort person från samlingen om den finns.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Skapa en personsamling med två personer.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Ta bort en person från samlingen med indexet.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Ta bort alla personer från samlingen.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Se även

* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
## PersonCollection::PersonCollection(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\&) constructor


Initiera en ny instans av klassen [PersonCollection](../).

```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection(const System::ArrayPtr<System::SharedPtr<Aspose::Words::Bibliography::Person>> &persons)
```


## Exempel



Visar hur man arbetar med personsamlingen.
```cpp
// Skapa en ny personsamling.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Lägg till en ny person i samlingen.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Ta bort person från samlingen om den finns.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Skapa en personsamling med två personer.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Ta bort en person från samlingen med indexet.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Ta bort alla personer från samlingen.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Se även

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
## PersonCollection::PersonCollection(const System::SharedPtr\<System::Collections::Generic::IEnumerable\<System::SharedPtr\<Aspose::Words::Bibliography::Person\>\>\>\&) constructor




```cpp
Aspose::Words::Bibliography::PersonCollection::PersonCollection(const System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Bibliography::Person>>> &persons)
```

## Se även

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
