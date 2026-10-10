---
title: "Metodo get_Value di Aspose::Words::Markup::SdtListItem"
linktitle: "get_Value"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_Value di Aspose::Words::Markup::SdtListItem. Ottiene il valore di questo elemento di elenco in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.markup/sdtlistitem/get_value/
---
## SdtListItem::get_Value method


Ottiene il valore di questo elemento di elenco.

```cpp
System::String Aspose::Words::Markup::SdtListItem::get_Value() const
```

## Note


Non può essere **null** e non può essere una stringa vuota.

## Esempi



Mostra come lavorare con i tag di documento strutturato a elenco a discesa.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::DropDownList, Aspose::Words::Markup::MarkupLevel::Block);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

// Un tag di documento strutturato a elenco a discesa è un modulo che consente all'utente di
// selezionare un'opzione da un elenco facendo clic con il tasto sinistro e aprendo il modulo in Microsoft Word.
// La proprietà "ListItems" contiene tutti gli elementi di elenco, e ogni elemento di elenco è un "SdtListItem".
System::SharedPtr<Aspose::Words::Markup::SdtListItemCollection> listItems = tag->get_ListItems();
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Value 1"));

ASSERT_EQ(listItems->idx_get(0)->get_DisplayText(), listItems->idx_get(0)->get_Value());

// Aggiungi altri 3 elementi di elenco. Inizializza questi elementi usando un costruttore diverso rispetto al primo elemento
// per visualizzare stringhe diverse dai loro valori.
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 2", u"Value 2"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 3", u"Value 3"));
listItems->Add(System::MakeObject<Aspose::Words::Markup::SdtListItem>(u"Item 4", u"Value 4"));

ASSERT_EQ(4, listItems->get_Count());

// L'elenco a discesa mostra il primo elemento. Assegna un elemento diverso dell'elenco a "SelectedValue" per visualizzarlo.
listItems->set_SelectedValue(listItems->idx_get(3));

ASSERT_EQ(u"Value 4", listItems->get_SelectedValue()->get_Value());

// Enumera la collezione e stampa ogni elemento.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::SdtListItem>>> enumerator = listItems->GetEnumerator();
    while (enumerator->MoveNext())
    {
        if (enumerator->get_Current() != nullptr)
        {
            std::cout << System::String::Format(u"List item: {0}, value: {1}", enumerator->get_Current()->get_DisplayText(), enumerator->get_Current()->get_Value()) << std::endl;
        }
    }
}

// Rimuovi l'ultimo elemento dell'elenco.
listItems->RemoveAt(3);

ASSERT_EQ(3, listItems->get_Count());

// Poiché il nostro controllo a discesa è impostato per visualizzare l'elemento rimosso per impostazione predefinita, fornisci un elemento da visualizzare che esista.
listItems->set_SelectedValue(listItems->idx_get(1));

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.ListItemCollection.docx");

// Usa il metodo "Clear" per svuotare l'intera collezione di elementi a discesa in una volta.
listItems->Clear();

ASSERT_EQ(0, listItems->get_Count());
```

## Vedi anche

* Class [SdtListItem](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
