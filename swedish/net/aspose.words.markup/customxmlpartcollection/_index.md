---
title: CustomXmlPartCollection Class
linktitle: CustomXmlPartCollection
articleTitle: CustomXmlPartCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Markup.CustomXmlPartCollection, din lösning för att hantera anpassade XML-delar effektivt och enkelt.
type: docs
weight: 4620
url: /sv/net/aspose.words.markup/customxmlpartcollection/
---
## CustomXmlPartCollection class

Representerar en samling anpassade XML-delar. Objekten är[`CustomXmlPart`](../customxmlpart/) objekt.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class CustomXmlPartCollection : IEnumerable<CustomXmlPart>
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CustomXmlPartCollection](customxmlpartcollection/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpartcollection/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | Hämtar eller ställer in ett objekt vid det angivna indexet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(*[CustomXmlPart](../customxmlpart/)*) | Lägger till ett objekt i samlingen. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(*string, string*) | Skapar en ny XML-del med den angivna XML-filen och lägger till den i samlingen. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | Tar bort alla element från samlingen. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | Skapar en djup kopia av den här samlingen och dess objekt. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(*string*) | Hittar och returnerar en anpassad XML-del med hjälp av dess identifierare. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | Returnerar ett uppräknarobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(*int*) | Tar bort ett objekt vid det angivna indexet. |

## Anmärkningar

Normalt sett behöver du inte skapa instanser av den här klassen. Du kan komma åt anpassade XML-filer som lagras i ett dokument via[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) egendom.

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

* class [CustomXmlPart](../customxmlpart/)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
