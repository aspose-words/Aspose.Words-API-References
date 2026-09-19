---
title: "Aspose::Words::Fields::DropDownItemCollection::Insert metodo"
linktitle: "Inserisci"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::DropDownItemCollection::Insert metodo. Inserisce una stringa nella collezione all'indice specificato in C++."
type: docs
weight: 15000
url: /it/cpp/aspose.words.fields/dropdownitemcollection/insert/
---
## DropDownItemCollection::Insert method


Inserisce una stringa nella raccolta all'indice specificato.

```cpp
void Aspose::Words::Fields::DropDownItemCollection::Insert(int32_t index, const System::String &value)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice basato su zero al quale il valore viene inserito. |
| value | const System::String\& | La stringa da inserire. |

## Esempi



Mostra come inserire un campo casella combinata e modificare gli elementi nella sua raccolta di elementi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci una casella combinata e poi verifica la sua raccolta di elementi a discesa.
// In Microsoft Word, l'utente farà clic sulla casella combinata,
// e poi sceglierà uno degli elementi di testo nella raccolta da visualizzare.
System::ArrayPtr<System::String> items = System::MakeArray<System::String>({u"One", u"Two", u"Three"});
System::SharedPtr<Aspose::Words::Fields::FormField> comboBoxField = builder->InsertComboBox(u"DropDown", items, 0);
System::SharedPtr<Aspose::Words::Fields::DropDownItemCollection> dropDownItems = comboBoxField->get_DropDownItems();

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_EQ(u"One", dropDownItems->idx_get(0));
ASSERT_EQ(1, dropDownItems->IndexOf(u"Two"));
ASSERT_TRUE(dropDownItems->Contains(u"Three"));

// Esistono due modi per aggiungere un nuovo elemento a una raccolta esistente di elementi di casella a discesa.
// 1 -  Aggiungi un elemento alla fine della raccolta:
dropDownItems->Add(u"Four");

// 2 -  Inserisci un elemento prima di un altro elemento a un indice specificato:
dropDownItems->Insert(3, u"Three and a half");

ASSERT_EQ(5, dropDownItems->get_Count());

// Itera sulla raccolta e stampa ogni elemento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> dropDownCollectionEnumerator = dropDownItems->GetEnumerator();
    while (dropDownCollectionEnumerator->MoveNext())
    {
        std::cout << dropDownCollectionEnumerator->get_Current() << std::endl;
    }
}

// Esistono due modi per rimuovere elementi da una raccolta di elementi a discesa.
// 1 -  Rimuovi un elemento il cui contenuto è uguale alla stringa fornita:
dropDownItems->Remove(u"Four");

// 2 -  Rimuovi un elemento a un indice:
dropDownItems->RemoveAt(3);

ASSERT_EQ(3, dropDownItems->get_Count());
ASSERT_FALSE(dropDownItems->Contains(u"Three and a half"));
ASSERT_FALSE(dropDownItems->Contains(u"Four"));

doc->Save(get_ArtifactsDir() + u"FormFields.DropDownItemCollection.html");

// Svuota l'intera raccolta di elementi a discesa.
dropDownItems->Clear();
```

## Vedi anche

* Class [DropDownItemCollection](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
