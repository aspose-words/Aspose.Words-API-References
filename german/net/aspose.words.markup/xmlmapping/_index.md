---
title: XmlMapping Class
linktitle: XmlMapping
articleTitle: XmlMapping
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Markup.XmlMapping, um strukturierte Dokument-Tags nahtlos mit XML-Elementen zu verknüpfen und so die Datenintegration Ihres Dokuments zu verbessern.
type: docs
weight: 4790
url: /de/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Gibt die Informationen an, die zum Erstellen einer Zuordnung zwischen dem übergeordneten strukturierten Dokumenttag und einem XML-Element verwendet werden, das in einem benutzerdefinierten XML-Datenteil im Dokument gespeichert ist.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class XmlMapping
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Gibt den benutzerdefinierten XML-Datenteil zurück, dem das übergeordnete strukturierte Dokument-Tag zugeordnet ist. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Rückgaben`WAHR` wenn das übergeordnete strukturierte Dokument-Tag erfolgreich XML-Daten zugeordnet wurde. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Gibt XML-Namespace-Präfix-Mappings zurück, um die[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Gibt den benutzerdefinierten XML-Datenbezeichner für den benutzerdefinierten XML-Datenteil an, der zur Auswertung der[`XPath`](./xpath/) Ausdruck. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Gibt den XPath-Ausdruck zurück, der ausgewertet wird, um den benutzerdefinierten XML-Knoten zu finden, der dem übergeordneten strukturierten Dokumenttag zugeordnet ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Löscht die Zuordnung des übergeordneten strukturierten Dokuments zu XML-Daten. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(*[CustomXmlPart](../customxmlpart/), string, string*) | Legt eine Zuordnung zwischen dem übergeordneten strukturierten Dokumenttag und einem XML-Knoten eines benutzerdefinierten XML-Datenteils fest. |

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
