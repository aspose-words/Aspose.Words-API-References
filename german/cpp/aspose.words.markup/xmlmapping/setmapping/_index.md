---
title: "Aspose::Words::Markup::XmlMapping::SetMapping Methode"
linktitle: "SetMapping"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::XmlMapping::SetMapping Methode. Legt eine Zuordnung zwischen dem übergeordneten structured document tag und einem XML-Knoten eines benutzerdefinierten XML-Datenparts in C++ fest."
type: docs
weight: 10000
url: /de/cpp/aspose.words.markup/xmlmapping/setmapping/
---
## XmlMapping::SetMapping method


Legt eine Zuordnung zwischen dem übergeordneten strukturierten Dokument-Tag und einem XML-Knoten eines benutzerdefinierten XML-Datenabschnitts fest.

```cpp
bool Aspose::Words::Markup::XmlMapping::SetMapping(const System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> &customXmlPart, const System::String &xPath, const System::String &prefixMapping)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| customXmlPart | const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\& | Ein benutzerdefinierter XML-Datenabschnitt, zu dem gemappt werden soll. |
| xPath | const System::String\& | Ein XPath-Ausdruck, um den XML-Knoten zu finden. |
| prefixMapping | const System::String\& | XML-Namespace-Präfixzuordnungen zur Auswertung des XPath. |

### ReturnValue

Ein Flag, das angibt, ob das übergeordnete strukturierte Dokument-Tag erfolgreich dem XML-Knoten zugeordnet ist.

## Beispiele



Zeigt, wie man ein strukturiertes Dokument-Tag mit benutzerdefinierten XML-Daten erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellt einen XML-Part, der Daten enthält, und fügt ihn zur Sammlung des Dokuments hinzu.
// Wenn wir die Registerkarte „Developer“ in Microsoft Word aktivieren,
// können wir Elemente aus dieser Sammlung im „XML Mapping Pane“ finden, zusammen mit einigen Standard-Elementen.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Hello world!</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASPOSE_ASSERT_EQ(System::Text::Encoding::get_ASCII()->GetBytes(xmlPartContent), xmlPart->get_Data());
ASSERT_EQ(xmlPartId, xmlPart->get_Id());

// Im Folgenden sind zwei Möglichkeiten aufgeführt, XML-Parts zu referenzieren.
// 1 -  Durch einen Index in der benutzerdefinierten XML-Part-Sammlung:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->idx_get(0));

// 2 -  Durch GUID:
ASPOSE_ASSERT_EQ(xmlPart, doc->get_CustomXmlParts()->GetById(xmlPartId));

// Fügen Sie eine XML-Schemazuordnung hinzu.
xmlPart->get_Schemas()->Add(u"http://www.w3.org/2001/XMLSchema");

// Klonen Sie einen Part und fügen Sie ihn anschließend in die Sammlung ein.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPartClone = xmlPart->Clone();
xmlPartClone->set_Id(System::Guid::NewGuid().ToString(u"B"));
doc->get_CustomXmlParts()->Add(xmlPartClone);

ASSERT_EQ(2, doc->get_CustomXmlParts()->get_Count());

// Iterieren Sie durch die Sammlung und geben Sie den Inhalt jedes Parts aus.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>> enumerator = doc->get_CustomXmlParts()->GetEnumerator();
    int32_t index = 0;
    while (enumerator->MoveNext())
    {
        std::cout << System::String::Format(u"XML part index {0}, ID: {1}", index, enumerator->get_Current()->get_Id()) << std::endl;
        std::cout << System::String::Format(u"\tContent: {0}", System::Text::Encoding::get_UTF8()->GetString(enumerator->get_Current()->get_Data())) << std::endl;
        index++;
    }
}

// Verwenden Sie die Methode „RemoveAt“, um den geklonten Part anhand des Index zu entfernen.
doc->get_CustomXmlParts()->RemoveAt(1);

ASSERT_EQ(1, doc->get_CustomXmlParts()->get_Count());

// Klonen Sie die XML-Parts-Sammlung und verwenden Sie anschließend die Methode „Clear“, um alle Elemente auf einmal zu entfernen.
System::SharedPtr<Aspose::Words::Markup::CustomXmlPartCollection> customXmlParts = doc->get_CustomXmlParts()->Clone();
customXmlParts->Clear();

// Erstellen Sie ein strukturiertes Dokument-Tag, das den Inhalt unseres Parts anzeigt, und fügen Sie es in den Dokumentenkörper ein.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[1]", System::String::Empty);

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.CustomXml.docx");
```

## Siehe auch

* Class [CustomXmlPart](../../customxmlpart/)
* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
