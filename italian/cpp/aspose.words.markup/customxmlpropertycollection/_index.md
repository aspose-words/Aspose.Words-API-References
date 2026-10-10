---
title: "classe Aspose::Words::Markup::CustomXmlPropertyCollection"
linktitle: "CustomXmlPropertyCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Markup::CustomXmlPropertyCollection. Rappresenta una collezione di attributi XML personalizzati o proprietà di smart tag. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class


Rappresenta una raccolta di attributi XML personalizzati o proprietà di smart tag. Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlProperty\>\&) | Aggiunge una proprietà alla collezione. |
| [Clear](./clear/)() | Rimuove tutti gli elementi dalla collezione. |
| [Contains](./contains/)(const System::String\&) | Determina se la collezione contiene una proprietà con il nome specificato. |
| [get_Count](./get_count/)() | Ottiene il numero di elementi contenuti nella raccolta. |
| [GetEnumerator](./getenumerator/)() override | Restituisce un oggetto enumeratore che può essere usato per iterare su tutti gli elementi della raccolta. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Ottiene una proprietà con il nome specificato. |
| [idx_get](./idx_get/)(int32_t) | Ottiene una proprietà all'indice specificato. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Restituisce l'indice basato su zero della proprietà specificata nella collezione. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Rimuove una proprietà con il nome specificato dalla raccolta. |
| [RemoveAt](./removeat/)(int32_t) | Rimuove una proprietà all'indice specificato. |
| static [Type](./type/)() |  |
## Note


Gli elementi sono oggetti [CustomXmlProperty](../customxmlproperty/).

## Esempi



Mostra come lavorare con le proprietà dei smart tag per ottenere informazioni approfondite sui smart tag.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// Un smart tag appare in un documento in cui Microsoft Word riconosce una parte del suo testo come una forma di dati,
// come un nome, una data o un indirizzo, e lo converte in un collegamento ipertestuale che mostra una sottolineatura punteggiata viola.
// In Word 2003, possiamo abilitare i smart tag tramite "Tools" -> "AutoCorrect options..." -> "SmartTags".
// Nel nostro documento di input, ci sono tre oggetti che Microsoft Word ha registrato come smart tag.
// I smart tag possono essere nidificati, quindi questa collezione ne contiene di più.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// Il membro "Properties" di un smart tag contiene i suoi metadati, che saranno diversi per ogni tipo di smart tag.
// Le proprietà di un smart tag di tipo "date" contengono l'anno, il mese e il giorno.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPropertyCollection> properties = smartTags[7]->get_Properties();

ASSERT_EQ(4, properties->get_Count());

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> enumerator = properties->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"Property name: {0}, value: {1}", enumerator->get_Current()->get_Name(), enumerator->get_Current()->get_Value()) << std::endl;
        ASSERT_EQ(u"", enumerator->get_Current()->get_Uri());
    }
}

// Possiamo anche accedere alle proprietà in vari modi, ad esempio come coppia chiave-valore.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// Di seguito sono riportati tre modi per rimuovere elementi dalla collezione di proprietà.
// 1 -  Rimuovi per indice:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  Rimuovi per nome:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Svuota l'intera collezione in una volta:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Vedi anche

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
