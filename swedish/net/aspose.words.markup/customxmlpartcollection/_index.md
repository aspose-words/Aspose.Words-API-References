---
title: CustomXmlPartCollection Class
linktitle: CustomXmlPartCollection
articleTitle: CustomXmlPartCollection
second_title: Aspose.Words för .NET
description: Aspose.Words.Markup.CustomXmlPartCollection klass. Representerar en samling anpassade XMLdelar. Objekten ärCustomXmlPart objekt i C#.
type: docs
weight: 3930
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
| [Item](../../aspose.words.markup/customxmlpartcollection/item/) { get; set; } | Hämtar eller ställer in ett objekt på angivet index. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add_1)(*[CustomXmlPart](../customxmlpart/)*) | Lägger till ett föremål i samlingen. |
| [Add](../../aspose.words.markup/customxmlpartcollection/add/#add)(*string, string*) | Skapar en ny XML-del med angiven XML och lägger till den i samlingen. |
| [Clear](../../aspose.words.markup/customxmlpartcollection/clear/)() | Tar bort alla element från samlingen. |
| [Clone](../../aspose.words.markup/customxmlpartcollection/clone/)() | Gör en djup kopia av den här samlingen och dess föremål. |
| [GetById](../../aspose.words.markup/customxmlpartcollection/getbyid/)(*string*) | Hittar och returnerar en anpassad XML-del med dess identifierare. |
| [GetEnumerator](../../aspose.words.markup/customxmlpartcollection/getenumerator/)() | Returnerar ett uppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [RemoveAt](../../aspose.words.markup/customxmlpartcollection/removeat/)(*int*) | Tar bort ett objekt vid angivet index. |

## Anmärkningar

Du behöver normalt inte skapa instanser av den här klassen. Du kan komma åt anpassade XML-data lagrade i ett dokument via[`CustomXmlParts`](../../aspose.words/document/customxmlparts/) fast egendom.

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

* class [CustomXmlPart](../customxmlpart/)
* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
