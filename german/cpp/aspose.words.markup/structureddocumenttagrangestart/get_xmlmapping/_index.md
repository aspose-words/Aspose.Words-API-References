---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping Methode"
linktitle: "get_XmlMapping"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping Methode. Gibt ein Objekt zurück, das die Zuordnung dieses strukturierten Dokumenten-Tag‑Bereichs zu XML‑Daten in einem benutzerdefinierten XML‑Teil des aktuellen Dokuments in C++ darstellt."
type: docs
weight: 21000
url: /de/cpp/aspose.words.markup/structureddocumenttagrangestart/get_xmlmapping/
---
## StructuredDocumentTagRangeStart::get_XmlMapping method


Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokumenten‑Tag‑Bereichs zu XML‑Daten in einem benutzerdefinierten XML‑Teil des aktuellen Dokuments darstellt.

```cpp
System::SharedPtr<Aspose::Words::Markup::XmlMapping> Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_XmlMapping() override
```


## Beispiele



Zeigt, wie man XML‑Zuordnungen für den Bereichsstart eines strukturierten Dokumenten‑Tags festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

// Erstellen Sie einen XML-Teil, der Text enthält, und fügen Sie ihn zur CustomXmlPart‑Sammlung des Dokuments hinzu.
System::String xmlPartId = System::Guid::NewGuid().ToString(u"B");
System::String xmlPartContent = u"<root><text>Text element #1</text><text>Text element #2</text></root>";
System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(xmlPartId, xmlPartContent);

ASSERT_EQ(u"<root><text>Text element #1</text><text>Text element #2</text></root>", System::Text::Encoding::get_UTF8()->GetString(xmlPart->get_Data()));

// Erstellen Sie einen strukturierten Dokumenten‑Tag, der den Inhalt unseres CustomXmlPart im Dokument anzeigt.
auto sdtRangeStart = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, 0, true));

// Wenn wir eine Zuordnung für unseren strukturierten Dokumenten‑Tag festlegen,
// wird er nur einen Teil des CustomXmlPart anzeigen, auf den der XPath verweist.
// Dieser XPath verweist auf das zweite "<text>"‑Element des ersten "<root>"‑Elements unseres CustomXmlPart.
sdtRangeStart->get_XmlMapping()->SetMapping(xmlPart, u"/root[1]/text[2]", nullptr);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

## Siehe auch

* Class [XmlMapping](../../xmlmapping/)
* Class [StructuredDocumentTagRangeStart](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
