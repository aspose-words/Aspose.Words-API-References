---
title: "Aspose::Words::Markup::CustomXmlPart class"
linktitle: "CustomXmlPart"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::CustomXmlPart Klasse. Stellt ein Custom XML Data Storage Part (benutzerdefinierte XML-Daten innerhalb eines Pakets) dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.markup/customxmlpart/
---
## CustomXmlPart class


Stellt einen Custom XML Data Storage Part (benutzerdefinierte XML-Daten innerhalb eines Pakets) dar. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPart : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clone](./clone/)() | Erstellt eine „deep enough“-Kopie des Objekts. Dupliziert nicht die Bytes des [Data](./get_data/)-Werts. |
| [CustomXmlPart](./customxmlpart/)() |  |
| [get_Data](./get_data/)() const | Liest oder setzt den XML-Inhalt dieses Custom XML Data Storage Parts. |
| [get_DataChecksum](./get_datachecksum/)() | Gibt eine zyklische Redundanzprüfung (CRC)-Prüfsumme des [Data](./get_data/)-Inhalts an. |
| [get_Id](./get_id/)() const | Liest oder setzt die Zeichenkette, die diesen benutzerdefinierten XML-Part in einem OOXML-Dokument identifiziert. |
| [get_Schemas](./get_schemas/)() const | Gibt die Menge der XML-Schemas an, die mit diesem benutzerdefinierten XML-Part verknüpft sind. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Data](./set_data/)(const System::ArrayPtr\<uint8_t\>\&) | Setter für [Aspose::Words::Markup::CustomXmlPart::get_Data](./get_data/). |
| [set_Id](./set_id/)(const System::String\&) | Setter für [Aspose::Words::Markup::CustomXmlPart::get_Id](./get_id/). |
| static [Type](./type/)() |  |
## Hinweise


Ein DOCX- oder DOC-Dokument kann einen oder mehrere Custom XML Data Storage Parts enthalten. Aspose.Words bewahrt und ermöglicht das Erstellen und Extrahieren von Custom XML Data über die [CustomXmlParts](../../aspose.words/document/get_customxmlparts/) Sammlung.

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

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
