---
title: CustomPart.RelationshipType
second_title: Aspose.Words für .NET-API-Referenz
description: CustomPart eigendom. Ruft den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil ab oder legt ihn fest.
type: docs
weight: 60
url: /de/net/aspose.words.markup/custompart/relationshiptype/
---
## CustomPart.RelationshipType property

Ruft den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil ab oder legt ihn fest.

```csharp
public string RelationshipType { get; set; }
```

### Bemerkungen

Der Beziehungstyp für ein benutzerdefiniertes Teil muss "unbekannt" sein, z. B. ein benutzerdefinierter Beziehungstyp, und keiner der in ISO/IEC 29500 definierten Beziehungstypen.

Der Standardwert ist eine leere Zeichenfolge. Ein gültiger Wert muss eine nicht leere Zeichenfolge sein.

### Beispiele

Zeigt, wie auf die Sammlung beliebiger benutzerdefinierter Teile eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Den zweiten Teil klonen, dann den Klon zur Sammlung hinzufügen.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Aufzählen über die Sammlung und jeden Teil drucken.
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

// Wir können Elemente aus dieser Sammlung einzeln oder alle auf einmal entfernen.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### Siehe auch

* class [CustomPart](../)
* namensraum [Aspose.Words.Markup](../../custompart/)
* Montage [Aspose.Words](../../../)


