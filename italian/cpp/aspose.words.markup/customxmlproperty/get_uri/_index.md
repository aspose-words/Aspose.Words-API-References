---
title: "Aspose::Words::Markup::CustomXmlProperty::get_Uri metodo"
linktitle: "get_Uri"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::CustomXmlProperty::get_Uri metodo. Ottiene o imposta l'URI dello spazio dei nomi dell'attributo XML personalizzato o della proprietà di smart tag in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.markup/customxmlproperty/get_uri/
---
## CustomXmlProperty::get_Uri method


Ottiene o imposta l'URI dello spazio dei nomi dell'attributo XML personalizzato o della proprietà di smart tag.

```cpp
System::String Aspose::Words::Markup::CustomXmlProperty::get_Uri() const
```

## Note


Non può essere **null**.

Il valore predefinito è una stringa vuota.

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

* Class [CustomXmlProperty](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
