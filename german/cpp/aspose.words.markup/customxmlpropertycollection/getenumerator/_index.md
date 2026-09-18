---
title: "Aspose::Words::Markup::CustomXmlPropertyCollection::GetEnumerator Methode"
linktitle: "GetEnumerator"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::CustomXmlPropertyCollection::GetEnumerator Methode. Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente der Sammlung in C++ zu iterieren."
type: docs
weight: 6000
url: /de/cpp/aspose.words.markup/customxmlpropertycollection/getenumerator/
---
## CustomXmlPropertyCollection::GetEnumerator method


Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlProperty>>> Aspose::Words::Markup::CustomXmlPropertyCollection::GetEnumerator() override
```


## Beispiele



Zeigt, wie man mit Smart‑Tag‑Eigenschaften arbeitet, um detaillierte Informationen zu Smart‑Tags zu erhalten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Smart tags.doc");

// Ein Smart‑Tag erscheint in einem Dokument, wenn Microsoft Word einen Teil seines Textes als eine Art Daten erkennt,
// wie einen Namen, ein Datum oder eine Adresse, und wandelt ihn in einen Hyperlink um, der eine lila gepunktete Unterstreichung anzeigt.
// In Word 2003 können wir Smart‑Tags über "Tools" → "AutoCorrect options..." → "SmartTags" aktivieren.
// In unserem Eingabedokument gibt es drei Objekte, die Microsoft Word als Smart‑Tags registriert hat.
// Smart‑Tags können verschachtelt sein, sodass diese Sammlung mehr enthält.
System::ArrayPtr<System::SharedPtr<Aspose::Words::Markup::SmartTag>> smartTags = doc->GetChildNodes(Aspose::Words::NodeType::SmartTag, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Markup::SmartTag> >()->LINQ_ToArray();

ASSERT_EQ(8, smartTags->get_Length());

// Das "Properties"-Element eines SmartTags enthält seine Metadaten, die für jeden Typ von SmartTag unterschiedlich sein werden.
// Die Eigenschaften eines "date"-Typ‑SmartTags enthalten sein Jahr, Monat und Tag.
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

// Wir können auch auf die Eigenschaften auf verschiedene Arten zugreifen, zum Beispiel als Schlüssel‑Wert‑Paar.
ASSERT_TRUE(properties->Contains(u"Day"));
ASSERT_EQ(u"22", properties->idx_get(u"Day")->get_Value());
ASSERT_EQ(u"2003", properties->idx_get(2)->get_Value());
ASSERT_EQ(1, properties->IndexOfKey(u"Month"));

// Im Folgenden sind drei Methoden zum Entfernen von Elementen aus der Eigenschaften‑Sammlung aufgeführt.
// 1 -  Entfernen nach Index:
properties->RemoveAt(3);

ASSERT_EQ(3, properties->get_Count());

// 2 -  Entfernen nach Name:
properties->Remove(u"Year");

ASSERT_EQ(2, properties->get_Count());

// 3 -  Lösche die gesamte Sammlung auf einmal:
properties->Clear();

ASSERT_EQ(0, properties->get_Count());
```

## Siehe auch

* Class [CustomXmlProperty](../../customxmlproperty/)
* Class [CustomXmlPropertyCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
