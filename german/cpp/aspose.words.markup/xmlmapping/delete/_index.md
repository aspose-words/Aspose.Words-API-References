---
title: "Aspose::Words::Markup::XmlMapping::Delete method"
linktitle: "Löschen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::XmlMapping::Delete method. Löscht die Zuordnung des übergeordneten strukturierten Dokuments zu XML-Daten in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.markup/xmlmapping/delete/
---
## XmlMapping::Delete method


Löscht die Zuordnung des übergeordneten strukturierten Dokuments zu XML-Daten.

```cpp
void Aspose::Words::Markup::XmlMapping::Delete()
```


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

* Class [XmlMapping](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
