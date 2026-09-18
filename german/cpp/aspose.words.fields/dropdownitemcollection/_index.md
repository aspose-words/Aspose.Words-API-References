---
title: "Aspose::Words::Fields::DropDownItemCollection Klasse"
linktitle: "DropDownItemCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::DropDownItemCollection Klasse. Eine Sammlung von Zeichenketten, die alle Elemente eines Dropdown-Formularfelds darstellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


Eine Sammlung von Zeichenketten, die alle Elemente eines Dropdown‑Formularfelds darstellen. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::String\&) | Fügt eine Zeichenkette am Ende der Sammlung hinzu. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Contains](./contains/)(const System::String\&) | Bestimmt, ob die Sammlung den angegebenen Wert enthält. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Liefert oder setzt das Element am angegebenen Index. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Liefert oder setzt das Element am angegebenen Index. |
| [IndexOf](./indexof/)(const System::String\&) | Gibt den nullbasierten Index des angegebenen Wertes in der Sammlung zurück. |
| [Insert](./insert/)(int32_t, const System::String\&) | Fügt eine Zeichenkette an der angegebenen Position in die Sammlung ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Entfernt den angegebenen Wert aus der Sammlung. |
| [RemoveAt](./removeat/)(int32_t) | Entfernt einen Wert am angegebenen Index. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
