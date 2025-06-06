---
title: CustomPart.RelationshipType
linktitle: RelationshipType
articleTitle: RelationshipType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „CustomPart RelationshipType“, um Beziehungen zwischen übergeordneten und benutzerdefinierten Teilen einfach zu verwalten und zu definieren und so die Funktionalität zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.markup/custompart/relationshiptype/
---
## CustomPart.RelationshipType property

Ruft den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil ab oder legt ihn fest.

```csharp
public string RelationshipType { get; set; }
```

## Bemerkungen

Der Beziehungstyp für ein benutzerdefiniertes Teil muss „unbekannt“ sein, z. B. ein benutzerdefinierter Beziehungstyp, und nicht einer der in ISO/IEC 29500 definierten Beziehungstypen.

Der Standardwert ist eine leere Zeichenfolge. Ein gültiger Wert darf keine leere Zeichenfolge sein.

## Beispiele

Zeigt, wie auf die beliebige benutzerdefinierte Teilesammlung eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Klonen Sie den zweiten Teil und fügen Sie den Klon dann der Sammlung hinzu.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Die Sammlung aufzählen und jeden Teil drucken.
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

// Wir können Elemente einzeln oder alle auf einmal aus dieser Sammlung entfernen.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Siehe auch

* class [CustomPart](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
