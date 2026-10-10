---
title: "Aspose::Words::Markup::XmlMapping Klasse"
linktitle: "XmlMapping"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::XmlMapping Klasse. Gibt die Informationen an, die verwendet werden, um eine Zuordnung zwischen dem übergeordneten strukturierten Dokument-Tag und einem XML-Element, das in einem benutzerdefinierten XML-Datenabschnitt im Dokument gespeichert ist, herzustellen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.markup/xmlmapping/
---
## XmlMapping class


Gibt die Informationen an, die verwendet werden, um eine Zuordnung zwischen dem übergeordneten strukturierten Dokument‑Tag und einem XML‑Element, das in einem benutzerdefinierten XML‑Datenabschnitt im Dokument gespeichert ist, herzustellen. Weitere Informationen finden Sie im Dokumentationsartikel [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class XmlMapping : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Delete](./delete/)() | Löscht die Zuordnung des übergeordneten strukturierten Dokuments zu XML-Daten. |
| [get_CustomXmlPart](./get_customxmlpart/)() | Gibt den benutzerdefinierten XML-Datenabschnitt zurück, dem der übergeordnete strukturierte Dokument-Tag zugeordnet ist. |
| [get_IsMapped](./get_ismapped/)() | Gibt **true** zurück, wenn der übergeordnete strukturierte Dokument-Tag erfolgreich zu XML-Daten zugeordnet wurde. |
| [get_PrefixMappings](./get_prefixmappings/)() const | Gibt XML-Namespace-Präfixzuordnungen zurück, um den [XPath](./get_xpath/) auszuwerten. |
| [get_StoreItemId](./get_storeitemid/)() | Gibt den benutzerdefinierten XML-Daten-Identifikator für den benutzerdefinierten XML-Datenabschnitt an, der zur Auswertung des [XPath](./get_xpath/) Ausdrucks verwendet werden soll. |
| [get_XPath](./get_xpath/)() const | Gibt den XPath-Ausdruck zurück, der ausgewertet wird, um den benutzerdefinierten XML-Knoten zu finden, der dem übergeordneten strukturierten Dokument-Tag zugeordnet ist. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [SetMapping](./setmapping/)(const System::SharedPtr\<Aspose::Words::Markup::CustomXmlPart\>\&, const System::String\&, const System::String\&) | Legt eine Zuordnung zwischen dem übergeordneten strukturierten Dokument-Tag und einem XML-Knoten eines benutzerdefinierten XML-Datenabschnitts fest. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man XML-Zuordnungen für benutzerdefinierte XML-Teile festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstellen Sie einen XML-Teil, der Text enthält, und fügen Sie ihn zur CustomXmlPart‑Sammlung des Dokuments hinzu.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Erstellen Sie einen strukturierten Dokument-Tag, der den Inhalt unseres CustomXmlPart anzeigt.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Block);

// Legen Sie eine Zuordnung für unseren strukturierten Dokument-Tag fest. Diese Zuordnung wird anweisen
// unseren strukturierten Dokument-Tag, einen Teil des Textinhalts des XML-Teils anzuzeigen, auf den der XPath verweist.
// In diesem Fall wird es der Inhalt des zweiten \"<text>\"-Elements des ersten \"<root>\"-Elements sein: \"Text element #2\".
tag->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", u"xmlns:ns='http://www.w3.org/2001/XMLSchema'");

ASSERT_TRUE(tag->get_XmlMapping()->get_IsMapped());
ASPOSE_ASSERT_EQ(xmlPart, tag->get_XmlMapping()->get_CustomXmlPart());
ASSERT_EQ(u"/root[1]/text[2]", tag->get_XmlMapping()->get_XPath());
ASSERT_EQ(u"xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag->get_XmlMapping()->get_PrefixMappings());

// Fügen Sie dem Dokument das strukturierte Dokument-Tag hinzu, um den Inhalt aus unserem benutzerdefinierten Teil anzuzeigen.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(tag);
doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.XmlMapping.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
