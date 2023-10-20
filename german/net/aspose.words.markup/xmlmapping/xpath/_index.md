---
title: XmlMapping.XPath
linktitle: XPath
articleTitle: XPath
second_title: Aspose.Words für .NET
description: XmlMapping XPath eigendom. Gibt den XPathAusdruck zurück der ausgewertet wird um den benutzerdefinierten XMLKnoten zu finden der dem Tag des übergeordneten strukturierten Dokuments zugeordnet ist in C#.
type: docs
weight: 50
url: /de/net/aspose.words.markup/xmlmapping/xpath/
---
## XmlMapping.XPath property

Gibt den XPath-Ausdruck zurück, der ausgewertet wird, um den benutzerdefinierten XML-Knoten zu finden, der dem Tag des übergeordneten strukturierten Dokuments zugeordnet ist.

```csharp
public string XPath { get; }
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

// Legen Sie eine Zuordnung für unser strukturiertes Dokument-Tag fest. Diese Zuordnung wird Ihnen Anweisungen geben
// unser strukturiertes Dokument-Tag, um einen Teil des Textinhalts des XML-Teils anzuzeigen, auf den der XPath verweist.
// In diesem Fall handelt es sich um den Inhalt des zweiten „<text>“ Element des ersten „<root>“ Element: „Textelement #2“.
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[2]", "xmlns:ns='http://www.w3.org/2001/XMLSchema'");

Assert.True(tag.XmlMapping.IsMapped);
Assert.AreEqual(xmlPart, tag.XmlMapping.CustomXmlPart);
Assert.AreEqual("/root[1]/text[2]", tag.XmlMapping.XPath);
Assert.AreEqual("xmlns:ns='http://www.w3.org/2001/XMLSchema'", tag.XmlMapping.PrefixMappings);

// Fügen Sie dem Dokument das strukturierte Dokument-Tag hinzu, um den Inhalt unseres benutzerdefinierten Teils anzuzeigen.
doc.FirstSection.Body.AppendChild(tag);
doc.Save(ArtifactsDir + "StructuredDocumentTag.XmlMapping.docx");
```

### Siehe auch

* class [XmlMapping](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
