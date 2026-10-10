---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf‑metod"
linktitle: "IndexOf"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf‑metod. Returnerar det nollbaserade indexet för det angivna värdet i samlingen i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.markup/customxmlschemacollection/indexof/
---
## CustomXmlSchemaCollection::IndexOf method


Returnerar det nollbaserade indexet för det angivna värdet i samlingen.

```cpp
int32_t Aspose::Words::Markup::CustomXmlSchemaCollection::IndexOf(const System::String &value)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| value | const System::String\& | Det skiftlägeskänsliga värdet att hitta. |

### ReturnValue

Det nollbaserade indexet. Negativt värde om inte hittad.

## Exempel



Visar hur man arbetar med en XML-schema-samling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Lägg till en XML-schemaassociation.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Klona den anpassade XML-delens XML-schema-associationssamling,
// och lägg sedan till ett par nya scheman i klonen.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Iterera igenom schemana och skriv ut varje element.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Nedan följer tre sätt att ta bort scheman från samlingen.
// 1 -  Ta bort ett schema efter index:
schemas->RemoveAt(2);

// 2 -  Ta bort ett schema efter värde:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 -  Använd metoden "Clear" för att tömma samlingen på en gång.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Se även

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
