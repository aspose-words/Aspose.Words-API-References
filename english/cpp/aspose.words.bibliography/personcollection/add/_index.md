---
title: Aspose::Words::Bibliography::PersonCollection::Add method
linktitle: Add
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Bibliography::PersonCollection::Add method. Adds a Person to the collection in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.bibliography/personcollection/add/
---
## PersonCollection::Add method


Adds a [Person](../../person/) to the collection.

```cpp
void Aspose::Words::Bibliography::PersonCollection::Add(const System::SharedPtr<Aspose::Words::Bibliography::Person> &person)
```


| Parameter | Type | Description |
| --- | --- | --- |
| person | const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\& | The person to add to the collection. |

## Examples



Shows how to work with person collection. 
```cpp
// Create a new person collection.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Add new person to the collection.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Remove person from the collection if it exists.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Create person collection with two persons.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Remove person from the collection by the index.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Remove all persons from the collection.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## See Also

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
