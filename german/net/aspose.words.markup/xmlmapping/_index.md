---
title: Class XmlMapping
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Markup.XmlMapping klas. Gibt die Informationen an die zum Erstellen einer Zuordnung zwischen dem Tag des strukturierten Dokuments parent und einem XMLElement verwendet werden das in einem benutzerdefinierten XMLDatenteil im Dokument gespeichert ist.
type: docs
weight: 4100
url: /de/net/aspose.words.markup/xmlmapping/
---
## XmlMapping class

Gibt die Informationen an, die zum Erstellen einer Zuordnung zwischen dem Tag des strukturierten Dokuments parent und einem XML-Element verwendet werden, das in einem benutzerdefinierten XML-Datenteil im Dokument gespeichert ist.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltskontrolle](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class XmlMapping
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CustomXmlPart](../../aspose.words.markup/xmlmapping/customxmlpart/) { get; } | Gibt den benutzerdefinierten XML-Datenteil zurück, dem das Tag des übergeordneten strukturierten Dokuments zugeordnet ist. |
| [IsMapped](../../aspose.words.markup/xmlmapping/ismapped/) { get; } | Gibt zurück`WAHR` wenn das Tag des übergeordneten strukturierten Dokuments erfolgreich XML-Daten zugeordnet wurde. |
| [PrefixMappings](../../aspose.words.markup/xmlmapping/prefixmappings/) { get; } | Gibt XML-Namespace-Präfixzuordnungen zur Auswertung zurück[`XPath`](./xpath/) . |
| [StoreItemId](../../aspose.words.markup/xmlmapping/storeitemid/) { get; } | Gibt die benutzerdefinierte XML-Datenkennung für den benutzerdefinierten XML-Datenteil an, der zur Auswertung verwendet werden soll[`XPath`](./xpath/) Ausdruck. |
| [XPath](../../aspose.words.markup/xmlmapping/xpath/) { get; } | Gibt den XPath-Ausdruck zurück, der ausgewertet wird, um den benutzerdefinierten XML-Knoten zu finden, der dem Tag des übergeordneten strukturierten Dokuments zugeordnet ist. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Delete](../../aspose.words.markup/xmlmapping/delete/)() | Löscht die Zuordnung des übergeordneten strukturierten Dokuments zu XML-Daten. |
| [SetMapping](../../aspose.words.markup/xmlmapping/setmapping/)(CustomXmlPart, string, string) | Legt eine Zuordnung zwischen dem Tag des übergeordneten strukturierten Dokuments und einem XML-Knoten eines benutzerdefinierten XML-Datenteils fest. |

### Beispiele

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)


