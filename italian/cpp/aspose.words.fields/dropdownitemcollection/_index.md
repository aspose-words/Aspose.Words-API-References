---
title: "Classe Aspose::Words::Fields::DropDownItemCollection"
linktitle: "DropDownItemCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Fields::DropDownItemCollection. Una raccolta di stringhe che rappresentano tutti gli elementi in un campo modulo a discesa. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class


Una raccolta di stringhe che rappresentano tutti gli elementi in un campo modulo a discesa. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class DropDownItemCollection : public System::Collections::Generic::IEnumerable<System::String>,
                               public Aspose::Words::IComplexAttr
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::String\&) | Aggiunge una stringa alla fine della raccolta. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [Contains](./contains/)(const System::String\&) | Determina se la raccolta contiene il valore specificato. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ottiene o imposta l'elemento all'indice specificato. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Ottiene o imposta l'elemento all'indice specificato. |
| [IndexOf](./indexof/)(const System::String\&) | Restituisce l'indice basato su zero del valore specificato nella raccolta. |
| [Insert](./insert/)(int32_t, const System::String\&) | Inserisce una stringa nella raccolta all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Rimuove il valore specificato dalla raccolta. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove un valore all'indice specificato. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Descrizione |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
