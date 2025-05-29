---
title: CustomXmlPart.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words för .NET
description: Upptäck hur du hanterar egenskapen CustomXmlPart Id för att enkelt identifiera och anpassa XML-delar i dina OOXML-dokument för förbättrad dokumenthantering.
type: docs
weight: 40
url: /sv/net/aspose.words.markup/customxmlpart/id/
---
## CustomXmlPart.Id property

Hämtar eller ställer in strängen som identifierar denna anpassade XML-del i ett OOXML-dokument.

```csharp
public string Id { get; set; }
```

## Anmärkningar

ISO/IEC 29500 anger att detta värde är ett GUID, men äldre versioner av Microsoft Word tillät vilken -sträng som helst här. Aspose.Words gör detsamma för ECMA-376-format. Observera dock att Microsoft Word Online misslyckas med att öppna ett dokument som skapats med ett värde som inte är ett GUID. Så ett GUID är ett föredraget värde för denna egenskap.

Ett giltigt värde måste vara en identifierare som är unik bland alla anpassade XML-datadelar i detta dokument.

Standardvärdet är en tom sträng. Värdet kan inte vara`null`.

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

* class [CustomXmlPart](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
