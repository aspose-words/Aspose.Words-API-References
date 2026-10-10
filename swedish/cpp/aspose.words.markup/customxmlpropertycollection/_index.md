---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection-klass"
linktitle: "CustomXmlPropertyCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection-klass. Representerar en samling av anpassade XML-attribut eller smarta taggegenskaper. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class


Representerar en samling av anpassade XML-attribut eller smart tag‑egenskaper. För att lära dig mer, besök dokumentationsartikeln [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPropertyCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlProperty\>\&) | Lägger till en egenskap i samlingen. |
| [Clear](./clear/)() | Tar bort alla element från samlingen. |
| [Contains](./contains/)(const System::String\&) | Avgör om samlingen innehåller en egenskap med det angivna namnet. |
| [get_Count](./get_count/)() | Hämtar antalet element som finns i samlingen. |
| [GetEnumerator](./getenumerator/)() override | Returnerar ett enumerator-objekt som kan användas för att iterera över alla objekt i samlingen. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Hämtar en egenskap med det angivna namnet. |
| [idx_get](./idx_get/)(int32_t) | Hämtar en egenskap på det angivna indexet. |
| [IndexOfKey](./indexofkey/)(const System::String\&) | Returnerar det nollbaserade indexet för den angivna egenskapen i samlingen. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::String\&) | Tar bort en egenskap med det angivna namnet från samlingen. |
| [RemoveAt](./removeat/)(int32_t) | Tar bort en egenskap på det angivna indexet. |
| static [Type](./type/)() |  |
## Anmärkningar


Objekten är [CustomXmlProperty](../customxmlproperty/) objekt.

## Exempel



Visar hur man arbetar med smarta taggegenskaper för att få djupgående information om smarta taggar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// En smart tag visas i ett dokument när Microsoft Word känner igen en del av dess text som någon form av data,
// såsom ett namn, datum eller adress, och konverterar den till en hyperlänk som visar en lila prickad understrykning.
// I Word 2003 kan vi aktivera smarta taggar via "Tools" -> "AutoCorrect options..." -> "SmartTags".
// I vårt inmatningsdokument finns tre objekt som Microsoft Word registrerade som smarta taggar.
// Smarta taggar kan vara nästlade, så den här samlingen innehåller fler.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// Medlemmen "Properties" i en smart tagg innehåller dess metadata, som kommer att vara olika för varje typ av smart tagg.
// Egenskaperna för en smart tagg av typen "date" innehåller dess år, månad och dag.
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

// Vi kan också komma åt egenskaperna på olika sätt, till exempel som ett nyckel‑värde‑par.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// Nedan följer tre sätt att ta bort element från egenskapskollektionen.
// 1 -  Ta bort efter index:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  Ta bort efter namn:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Rensa hela samlingen på en gång:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Se även

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
