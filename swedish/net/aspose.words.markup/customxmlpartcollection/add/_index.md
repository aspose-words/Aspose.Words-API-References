---
title: CustomXmlPartCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words för .NET
description: Upptäck CustomXmlPartCollection Add-metoden för att enkelt och effektivt förbättra dina samlingar genom att lägga till nya objekt.
type: docs
weight: 40
url: /sv/net/aspose.words.markup/customxmlpartcollection/add/
---
## Add(*[CustomXmlPart](../../customxmlpart/)*) {#add_1}

Lägger till ett objekt i samlingen.

```csharp
public void Add(CustomXmlPart part)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| part | CustomXmlPart | Den anpassade XML-delen som ska läggas till. |

## Exempel

Visar hur man skapar en strukturerad dokumenttagg med anpassad XML-data.

```csharp
Document doc = new Document();

// Konstruera en XML-del som innehåller data och lägg till den i dokumentets samling.
// Om vi aktiverar fliken "Utvecklare" i Microsoft Word,
// vi kan hitta element från den här samlingen i "XML-mappningsrutan", tillsammans med några standardelement.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Nedan följer två sätt att referera till XML-delar.
// 1 - Av ett index i den anpassade XML-delsamlingen:
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

// Använd metoden "RemoveAt" för att ta bort den klonade delen via index.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Klona XML-delsamlingen och använd sedan "Rensa"-metoden för att ta bort alla dess element på en gång.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Skapa en strukturerad dokumenttagg som visar innehållet i vår del och infogar den i dokumentets brödtext.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Se även

* class [CustomXmlPart](../../customxmlpart/)
* class [CustomXmlPartCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)

---

## Add(*string, string*) {#add}

Skapar en ny XML-del med den angivna XML-filen och lägger till den i samlingen.

```csharp
public CustomXmlPart Add(string id, string xml)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| id | String | Identifierare för en ny anpassad XML-del. |
| xml | String | XML-data för delen. |

### Returvärde

Skapade en anpassad XML-del.

## Exempel

Visar hur man skapar en strukturerad dokumenttagg med anpassad XML-data.

```csharp
Document doc = new Document();

// Konstruera en XML-del som innehåller data och lägg till den i dokumentets samling.
// Om vi aktiverar fliken "Utvecklare" i Microsoft Word,
// vi kan hitta element från den här samlingen i "XML-mappningsrutan", tillsammans med några standardelement.
string xmlPartId = Guid.NewGuid().ToString("B");
string xmlPartContent = "<root><text>Hello world!</text></root>";
CustomXmlPart xmlPart = doc.CustomXmlParts.Add(xmlPartId, xmlPartContent);

Assert.AreEqual(Encoding.ASCII.GetBytes(xmlPartContent), xmlPart.Data);
Assert.AreEqual(xmlPartId, xmlPart.Id);

// Nedan följer två sätt att referera till XML-delar.
// 1 - Av ett index i den anpassade XML-delsamlingen:
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

// Använd metoden "RemoveAt" för att ta bort den klonade delen via index.
doc.CustomXmlParts.RemoveAt(1);

Assert.AreEqual(1, doc.CustomXmlParts.Count);

// Klona XML-delsamlingen och använd sedan "Rensa"-metoden för att ta bort alla dess element på en gång.
CustomXmlPartCollection customXmlParts = doc.CustomXmlParts.Clone();
customXmlParts.Clear();

// Skapa en strukturerad dokumenttagg som visar innehållet i vår del och infogar den i dokumentets brödtext.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
tag.XmlMapping.SetMapping(xmlPart, "/root[1]/text[1]", string.Empty);

doc.FirstSection.Body.AppendChild(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.CustomXml.docx");
```

### Se även

* class [CustomXmlPart](../../customxmlpart/)
* class [CustomXmlPartCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
