---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection::IndexOfKey metod"
linktitle: "IndexOfKey"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection::IndexOfKey metod. Returnerar det nollbaserade indexet för den angivna egenskapen i samlingen i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.markup/customxmlpropertycollection/indexofkey/
---
## CustomXmlPropertyCollection::IndexOfKey method


Returnerar det nollbaserade indexet för den angivna egenskapen i samlingen.

```cpp
int32_t Aspose::Words::Markup::CustomXmlPropertyCollection::IndexOfKey(const System::String &name)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| namn | const System::String\& | Det skiftlägeskänsliga namnet på egenskapen. |

### ReturnValue

Det nollbaserade indexet. Negativt värde om inte hittad.

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

* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
