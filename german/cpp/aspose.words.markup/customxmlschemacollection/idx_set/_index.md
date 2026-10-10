---
title: "Aspose::Words::Markup::CustomXmlSchemaCollection::idx_set-Methode"
linktitle: "idx_set"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::CustomXmlSchemaCollection::idx_set-Methode. Ruft das Element am angegebenen Index ab oder legt es fest in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.markup/customxmlschemacollection/idx_set/
---
## CustomXmlSchemaCollection::idx_set method


Liefert oder setzt das Element am angegebenen Index.

```cpp
void Aspose::Words::Markup::CustomXmlSchemaCollection::idx_set(int32_t index, const System::String &value)
```


## Beispiele



Zeigt, wie man mit einer XML‑Schemata‑Sammlung arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello, World!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

// Fügen Sie eine XML-Schemazuordnung hinzu.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Klonen Sie die XML‑Schema‑Zuordnungs‑Sammlung des benutzerdefinierten XML‑Teils,
// und fügen Sie dann ein paar neue Schemata zum Klon hinzu.
System::SharedPtr<Aspose::Words::Markup::CustomXmlSchemaCollection> schemas = xmlPart->get_Schemas()->Clone();
schemas->Add(u"http://www.w3.org/2001/XMLSchema-instance");
schemas->Add(u"http://schemas.microsoft.com/office/2006/metadata/contentType");

ASSERT_EQ(3, schemas->get_Count());
ASSERT_EQ(2, schemas->IndexOf(u"http://schemas.microsoft.com/office/2006/metadata/contentType"));

// Durchlaufen Sie die Schemata und geben Sie jedes Element aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::String>> enumerator = schemas->GetEnumerator();
    while (enumerator->MoveNext())
    {
        std::cout << enumerator->get_Current() << std::endl;
    }
}

// Im Folgenden werden drei Methoden zum Entfernen von Schemata aus der Sammlung gezeigt.
// 1 - Entfernen Sie ein Schema nach Index:
schemas->RemoveAt(2);

// 2 - Entfernen Sie ein Schema nach Wert:
schemas->Remove(u"http://www.w3.org/2001/XMLSchema");

// 3 - Verwenden Sie die Methode "Clear", um die Sammlung auf einmal zu leeren.
schemas->Clear();

ASSERT_EQ(0, schemas->get_Count());
```

## Siehe auch

* Class [CustomXmlSchemaCollection](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
