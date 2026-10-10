---
title: "Aspose::Words::Fields::DropDownItemCollection::Clear Methode"
linktitle: "Clear"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::DropDownItemCollection::Clear Methode. Entfernt alle Elemente aus der Sammlung in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.fields/dropdownitemcollection/clear/
---
## DropDownItemCollection::Clear method


Entfernt alle Elemente aus der Sammlung.

```cpp
void Aspose::Words::Fields::DropDownItemCollection::Clear()
```


## Beispiele



Zeigt, wie man ein Kombinationsfeld einfügt und die Elemente seiner Elementsammlung bearbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Kombinationsfeld ein und überprüfen Sie anschließend seine Sammlung von Dropdown-Elementen.
// In Microsoft Word klickt der Benutzer das Kombinationsfeld,
// und wählt dann eines der Textelemente aus der Sammlung zur Anzeige aus.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// Es gibt zwei Möglichkeiten, ein neues Element zu einer bestehenden Sammlung von Dropdown-Box-Elementen hinzuzufügen.
// 1 -  Ein Element am Ende der Sammlung anhängen:
dropDownItems->Add(u"Four");

// 2 -  Ein Element vor einem anderen Element an einem angegebenen Index einfügen:
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Iterieren Sie über die Sammlung und geben Sie jedes Element aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// Es gibt zwei Möglichkeiten, Elemente aus einer Sammlung von Dropdown‑Einträgen zu entfernen.
// 1 -  Entferne ein Element, dessen Inhalt dem übergebenen String entspricht:
dropDownItems->Remove(u"Four");

// 2 -  Entferne ein Element an einem Index:
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Leere die gesamte Sammlung von Dropdown‑Einträgen.
dropDownItems->Clear();
```

## Siehe auch

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
