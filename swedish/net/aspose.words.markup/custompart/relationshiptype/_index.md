---
title: CustomPart.RelationshipType
linktitle: RelationshipType
articleTitle: RelationshipType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CustomPart RelationshipType för att enkelt hantera och definiera relationer mellan överordnade och anpassade delar för förbättrad funktionalitet.
type: docs
weight: 60
url: /sv/net/aspose.words.markup/custompart/relationshiptype/
---
## CustomPart.RelationshipType property

Hämtar eller anger relationstypen från förälderdelen till denna anpassade del.

```csharp
public string RelationshipType { get; set; }
```

## Anmärkningar

Relationstypen för en anpassad del måste vara "okänd", t.ex. en anpassad relationstyp, är inte en av de relationstyper som definieras i ISO/IEC 29500.

Standardvärdet är en tom sträng. Ett giltigt värde måste vara en sträng som inte är tom.

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

* class [CustomPart](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
