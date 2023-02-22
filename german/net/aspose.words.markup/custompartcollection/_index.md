---
title: Class CustomPartCollection
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Markup.CustomPartCollection klas. Repräsentiert eine Sammlung vonCustomPart Objekte.
type: docs
weight: 3670
url: /de/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

Repräsentiert eine Sammlung von[`CustomPart`](../custompart/) Objekte.

```csharp
public class CustomPartCollection : IEnumerable<CustomPart>
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CustomPartCollection](custompartcollection/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | Ruft ein Element am angegebenen Index ab oder legt es fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(CustomPart) | Fügt der Sammlung ein Element hinzu. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | Erstellt eine tiefe Kopie dieser Sammlung und ihrer Elemente. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | Gibt ein Aufzählungsobjekt zurück, das verwendet werden kann, um alle Elemente in der Sammlung zu durchlaufen. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(int) | Entfernt ein Element am angegebenen Index. |

### Bemerkungen

Normalerweise müssen Sie keine Instanzen dieser Klasse erstellen. Sie greifen über die auf benutzerdefinierte Teile zu, die sich auf das OOXML-Paket beziehen[`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) Eigentum.

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

* class [CustomPart](../custompart/)
* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)


