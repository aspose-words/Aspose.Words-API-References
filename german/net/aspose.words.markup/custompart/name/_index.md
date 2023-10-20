---
title: CustomPart.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words für .NET
description: CustomPart Name eigendom. Ruft den absoluten Namen dieses Teils innerhalb des OOXMLPakets oder der ZielURL ab oder legt diesen fest in C#.
type: docs
weight: 50
url: /de/net/aspose.words.markup/custompart/name/
---
## CustomPart.Name property

Ruft den absoluten Namen dieses Teils innerhalb des OOXML-Pakets oder der Ziel-URL ab oder legt diesen fest.

```csharp
public string Name { get; set; }
```

## Bemerkungen

Wenn das Beziehungsziel intern ist, ist diese Eigenschaft der absolute Teilname innerhalb des Pakets. Wenn das Beziehungsziel extern ist, ist diese Eigenschaft die Ziel-URL.

Der Standardwert ist eine leere Zeichenfolge. Ein gültiger Wert muss eine nicht leere Zeichenfolge sein.

## Beispiele

Zeigt, wie auf die beliebige benutzerdefinierte Teilesammlung eines Dokuments zugegriffen wird.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// Klonen Sie den zweiten Teil und fügen Sie dann den Klon zur Sammlung hinzu.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// Die Sammlung aufzählen und jeden Teil ausdrucken.
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
