---
title: Document.PackageCustomParts
linktitle: PackageCustomParts
articleTitle: PackageCustomParts
second_title: Aspose.Words för .NET
description: Hantera anpassade delar i ditt OOXML-paket utan ansträngning. Få enkel åtkomst till och modifiera länkat innehåll för förbättrad dokumentflexibilitet och funktionalitet.
type: docs
weight: 320
url: /sv/net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

Hämtar eller ställer in samlingen av anpassade delar (godtyckligt innehåll) som är länkade till OOXML-paketet med hjälp av "okända relationer".

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

## Anmärkningar

Förväxla inte dessa anpassade delar med anpassade XML-data. Om du behöver komma åt anpassade XML-delar, använd[`CustomXmlParts`](../customxmlparts/) egendom.

Denna samling innehåller OOXML-delar vars förälder är OOXML-paketet och deras mål är av en "okänd relation". För mer information, se[`CustomPart`](../../../aspose.words.markup/custompart/).

Aspose.Words laddar och sparar endast anpassade delar i OOXML-dokument.

Den här egenskapen kan inte vara`null`.

## Exempel

Visar hur man kommer åt ett dokuments godtyckliga samling av anpassade delar.

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

// Vi kan ta bort element från den här samlingen individuellt, eller alla på en gång.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Se även

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
