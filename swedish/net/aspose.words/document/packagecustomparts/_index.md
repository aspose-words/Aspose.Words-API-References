---
title: Document.PackageCustomParts
second_title: Aspose.Words för .NET API Referens
description: Document fast egendom. Hämtar eller ställer in samlingen av anpassade delar godtyckligt innehåll som är länkade till OOXMLpaketet med hjälp av okända relationer.
type: docs
weight: 290
url: /sv/net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

Hämtar eller ställer in samlingen av anpassade delar (godtyckligt innehåll) som är länkade till OOXML-paketet med hjälp av "okända relationer".

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

### Anmärkningar

Blanda inte ihop dessa anpassade delar med anpassade XML-data. Om du behöver komma åt anpassade XML-delar, använd[`CustomXmlParts`](../customxmlparts/) fast egendom.

Den här samlingen innehåller OOXML-delar vars överordnade är OOXML-paketet och deras mål har ett "okänt förhållande". För mer information se[`CustomPart`](../../../aspose.words.markup/custompart/).

Aspose.Words laddar och sparar endast anpassade delar i OOXML-dokument.

Den här egenskapen kan inte vara det`null`.

### Exempel

Visar hur man kommer åt ett dokuments godtyckliga anpassade delarsamling.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Klona den andra delen och lägg sedan till klonen i samlingen.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Räkna upp samlingen och skriv ut varje del.
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

// Vi kan ta bort element från denna samling individuellt eller alla på en gång.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Se även

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../document/)
* hopsättning [Aspose.Words](../../../)


