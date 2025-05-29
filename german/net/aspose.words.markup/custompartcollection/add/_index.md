---
title: CustomPartCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihr Projekt mühelos mit der Add-Methode „CustomPartCollection“ – fügen Sie Ihrer Sammlung schnell Elemente hinzu, um eine nahtlose Integration und Effizienz zu gewährleisten.
type: docs
weight: 40
url: /de/net/aspose.words.markup/custompartcollection/add/
---
## CustomPartCollection.Add method

Fügt der Sammlung ein Element hinzu.

```csharp
public void Add(CustomPart part)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| part | CustomPart | Das hinzuzufügende Element. |

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

* class [CustomPart](../../custompart/)
* class [CustomPartCollection](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
