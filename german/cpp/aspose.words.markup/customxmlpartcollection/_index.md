---
title: "Aspose::Words::Markup::CustomXmlPartCollection Klasse"
linktitle: "CustomXmlPartCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::CustomXmlPartCollection Klasse. Stellt eine Sammlung von Custom XML Parts dar. Die Elemente sind CustomXmlPart-Objekte. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class


Stellt eine Sammlung von Custom XML Parts dar. Die Elemente sind [CustomXmlPart](../customxmlpart/) Objekte. Weitere Informationen finden Sie im Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class CustomXmlPartCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::CustomXmlPart>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Fügt ein Element zur Sammlung hinzu. |
| [Add](./add/)(const System::String\&, const System::String\&) | Erstellt einen neuen XML-Teil mit dem angegebenen XML und fügt ihn der Sammlung hinzu. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Clone](./clone/)() | Erstellt eine tiefe Kopie dieser Sammlung und ihrer Elemente. |
| [CustomXmlPartCollection](./customxmlpartcollection/)() |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der in der Sammlung enthaltenen Elemente zurück. |
| [GetById](./getbyid/)(const System::String\&) | Findet und gibt einen benutzerdefinierten XML-Teil anhand seiner Kennung zurück. |
| [GetEnumerator](./getenumerator/)() override | Gibt ein Enumerator‑Objekt zurück, das verwendet werden kann, um über alle Elemente in der Sammlung zu iterieren. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Liest ein Element am angegebenen Index aus oder setzt es. |
| [idx_set](./idx_set/)(int32_t, const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&) | Liest ein Element am angegebenen Index aus oder setzt es. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [RemoveAt](./removeat/)(int32_t) | Entfernt ein Element am angegebenen Index. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |
## Hinweise


Normalerweise müssen Sie keine Instanzen dieser Klasse erstellen. Sie können auf benutzerdefinierte XML-Daten, die in einem Dokument gespeichert sind, über die Eigenschaft [CustomXmlParts](../../aspose.words/document/get_customxmlparts/) zugreifen.

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
