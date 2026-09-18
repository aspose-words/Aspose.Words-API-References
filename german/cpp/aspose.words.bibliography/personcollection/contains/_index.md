---
title: "Aspose::Words::Bibliography::PersonCollection::Contains Methode"
linktitle: "Contains"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Bibliography::PersonCollection::Contains Methode. Bestimmt, ob die Sammlung eine bestimmte Person enthält in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.bibliography/personcollection/contains/
---
## PersonCollection::Contains method


Bestimmt, ob die Sammlung eine bestimmte Person enthält.

```cpp
bool Aspose::Words::Bibliography::PersonCollection::Contains(const System::SharedPtr<Aspose::Words::Bibliography::Person> &person)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Person | const System::SharedPtr\<Aspose::Words::Bibliography::Person\>\& | Die zu findende Person in der Sammlung. |

## Beispiele



Zeigt, wie man mit einer Personensammlung arbeitet.
```cpp
// Erstelle eine neue Personensammlung.
auto persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>();
auto person = System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne", u"Brielle", u"Tejeda_updated");
// Füge eine neue Person zur Sammlung hinzu.
persons->Add(person);
ASSERT_EQ(1, persons->get_Count());
// Entferne die Person aus der Sammlung, falls sie existiert.
if (persons->Contains(person))
{
    persons->Remove(person);
}
ASSERT_EQ(0, persons->get_Count());

// Erstelle eine Personensammlung mit zwei Personen.
persons = System::MakeObject<Aspose::Words::Bibliography::PersonCollection>(System::MakeArray<System::SharedPtr<Aspose::Words::Bibliography::Person>>({System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_1", u"Brielle_1", u"Tejeda_1"), System::MakeObject<Aspose::Words::Bibliography::Person>(u"Roxanne_2", u"Brielle_2", u"Tejeda_2")}));
ASSERT_EQ(2, persons->get_Count());
// Entferne die Person aus der Sammlung anhand des Index.
persons->RemoveAt(0);
ASSERT_EQ(1, persons->get_Count());
// Entferne alle Personen aus der Sammlung.
persons->Clear();
ASSERT_EQ(0, persons->get_Count());
```

## Siehe auch

* Class [Person](../../person/)
* Class [PersonCollection](../)
* Namespace [Aspose::Words::Bibliography](../../)
* Library [Aspose.Words for C++](../../../)
