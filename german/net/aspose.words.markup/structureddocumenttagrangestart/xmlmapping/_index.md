---
title: StructuredDocumentTagRangeStart.XmlMapping
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die XmlMapping-Eigenschaft „StructuredDocumentTagRangeStart“ den Tag-Bereich Ihres Dokuments mit benutzerdefinierten XML-Daten verbindet und so die Dokumentintegration verbessert.
type: docs
weight: 190
url: /de/net/aspose.words.markup/structureddocumenttagrangestart/xmlmapping/
---
## StructuredDocumentTagRangeStart.XmlMapping property

Ruft ein Objekt ab, das die Zuordnung dieses strukturierten Dokument-Tag-Bereichs zu XML-Daten in einem benutzerdefinierten XML-Teil des aktuellen Dokuments darstellt.

```csharp
public XmlMapping XmlMapping { get; }
```

## Bemerkungen

Sie können die[`SetMapping`](../../xmlmapping/setmapping/) Methode dieses -Objekts, um einen strukturierten Dokument-Tag-Bereich XML-Daten zuzuordnen.

## Beispiele

Zeigt, wie XML-Zuordnungen für den Bereichsanfang eines strukturierten Dokumenttags festgelegt werden.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");

// Erstellen Sie einen XML-Teil, der Text enthält, und fügen Sie ihn der CustomXmlPart-Sammlung des Dokuments hinzu.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Erstellen Sie ein strukturiertes Dokument-Tag, das den Inhalt unseres CustomXmlPart im Dokument anzeigt.
StructuredDocumentTagRangeStart sdtRangeStart = (StructuredDocumentTagRangeStart)doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true);

// Wenn wir eine Zuordnung für unser strukturiertes Dokument-Tag festlegen,
// es wird nur ein Teil des CustomXmlPart angezeigt, auf den der XPath verweist.
// Dieser XPath zeigt auf den Inhalt des zweiten „<text>“-Elements des ersten „<root>“-Elements unseres CustomXmlPart.
sdtRangeStart.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", null);

doc.Save(ArtifactsDir + "StructuredDocumentTag.StructuredDocumentTagRangeStartXmlMapping.docx");
```

### Siehe auch

* class [XmlMapping](../../xmlmapping/)
* class [StructuredDocumentTagRangeStart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
