---
title: XmlMapping.IsMapped
linktitle: IsMapped
articleTitle: IsMapped
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die IsMapped-Eigenschaft von XmlMapping die XML-Datenzuordnung für strukturierte Dokumente effizient überprüft und so eine nahtlose Integration und Genauigkeit gewährleistet.
type: docs
weight: 20
url: /de/net/aspose.words.markup/xmlmapping/ismapped/
---
## XmlMapping.IsMapped property

Rückgaben`WAHR` wenn das übergeordnete strukturierte Dokument-Tag erfolgreich XML-Daten zugeordnet wurde.

```csharp
public bool IsMapped { get; }
```

## Beispiele

Zeigt, wie XML-Zuordnungen für benutzerdefinierte XML-Teile festgelegt werden.

```csharp
Document doc = new Document();

// Erstellen Sie einen XML-Teil, der Text enthält, und fügen Sie ihn der CustomXmlPart-Sammlung des Dokuments hinzu.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Text element #1</text><text>Text element #2</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual("<root><text>Text element #1</text><text>Text element #2</text></root>",
    Encoding.UTF8.GetString(xmlPart.Data));

// Erstellen Sie ein strukturiertes Dokument-Tag, das den Inhalt unseres CustomXmlPart anzeigt.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);

// Legen Sie eine Zuordnung für unser strukturiertes Dokument-Tag fest. Diese Zuordnung weist
// unser strukturiertes Dokument-Tag zum Anzeigen eines Teils des Textinhalts des XML-Teils, auf den der XPath verweist.
// In diesem Fall handelt es sich um den Inhalt des zweiten "<text>"-Elements des ersten "<root>"-Elements: "Textelement Nr. 2".
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// Fügen Sie dem Dokument das strukturierte Dokument-Tag hinzu, um den Inhalt aus unserem benutzerdefinierten Teil anzuzeigen.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Siehe auch

* class [XmlMapping](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
