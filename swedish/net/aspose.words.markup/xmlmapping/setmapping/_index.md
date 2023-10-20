---
title: XmlMapping.SetMapping
linktitle: SetMapping
articleTitle: SetMapping
second_title: Aspose.Words för .NET
description: XmlMapping SetMapping metod. Ställer in en mappning mellan den överordnade strukturerade dokumenttaggen och en XMLnod för en anpassad XMLdatadel i C#.
type: docs
weight: 70
url: /sv/net/aspose.words.markup/xmlmapping/setmapping/
---
## XmlMapping.SetMapping method

Ställer in en mappning mellan den överordnade strukturerade dokumenttaggen och en XML-nod för en anpassad XML-datadel.

```csharp
public bool SetMapping(CustomXmlPart customXmlPart, string xPath, string prefixMapping)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| customXmlPart | CustomXmlPart | En anpassad XML-datadel att mappa till. |
| xPath | String | Ett XPath-uttryck för att hitta XML-noden. |
| prefixMapping | String | XML-namnområdesprefixmappningar för att utvärdera XPath. |

### Returvärde

En flagga som indikerar om den överordnade strukturerade dokumenttaggen har mappats till XML-noden.

## Exempel

Visar hur man skapar en strukturerad dokumenttagg med anpassade XML-data.

```csharp
Document doc = new Document();

// Konstruera en XML-del som innehåller data och lägg till den i dokumentets samling.
// Om vi aktiverar fliken "Utvecklare" i Microsoft Word,
// vi kan hitta element från denna samling i "XML Mapping Pane", tillsammans med några standardelement.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Nedan finns två sätt att referera till XML-delar.
// 1 - Genom ett index i den anpassade XML-delsamlingen:
Assert.AreEqual(xmlPart, doc.CustomXmlParts[0]);

// 2 - Av GUID:
Assert.AreEqual(xmlPart, doc.CustomXmlParts.GetById(xmlPartId));

// Lägg till en XML-schemaassociation.
xmlPart.Schemas.Add("http://www.w3.org/2001/XMLSchema");

// Klona en del och infoga den sedan i samlingen.
CustomXmlPart xmlPartClone = xmlPart.Clone();
xmlPartClone.Id = Guid.NewGuid().ToString("B");
doc.CustomXmlParts.Add(xmlPartClone);

Assert.AreEqual(2, doc.CustomXmlParts.Count);

// Iterera genom samlingen och skriv ut innehållet i varje del.
using (IEnumerator<CustomXmlPart> enumerator = doc.CustomXmlParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"XML part index {index}, ID: {enumerator.Current.Id}");
        Console.WriteLine($"\tContent: {Encoding.UTF8.GetString(enumerator.Current.Data)}");
        index++;
    }
}

// Använd metoden "RemoveAt" för att ta bort den klonade delen efter index.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Klona XML-delsamlingen och använd sedan metoden "Rensa" för att ta bort alla dess element på en gång.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Skapa en strukturerad dokumenttagg som visar vår dels innehåll och infoga den i dokumentets brödtext.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Se även

* class [CustomXmlPart](../../customxmlpart/)
* class [XmlMapping](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
