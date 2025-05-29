---
title: CustomPartCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words för .NET
description: Förbättra ditt projekt enkelt med CustomPartCollection Add-metoden – lägg snabbt till objekt i din samling för sömlös integration och effektivitet.
type: docs
weight: 40
url: /sv/net/aspose.words.markup/custompartcollection/add/
---
## CustomPartCollection.Add method

Lägger till ett objekt i samlingen.

```csharp
public void Add(CustomPart part)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| part | CustomPart | Objektet som ska läggas till. |

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

* class [CustomPart](../../custompart/)
* class [CustomPartCollection](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
