---
title: Document.PackageCustomParts
linktitle: PackageCustomParts
articleTitle: PackageCustomParts
second_title: Aspose.Words für .NET
description: Verwalten Sie benutzerdefinierte Teile mühelos in Ihrem OOXML-Paket. Greifen Sie einfach auf verknüpfte Inhalte zu und ändern Sie diese, um die Flexibilität und Funktionalität Ihres Dokuments zu verbessern.
type: docs
weight: 320
url: /de/net/aspose.words/document/packagecustomparts/
---
## Document.PackageCustomParts property

Ruft die Sammlung benutzerdefinierter Teile (beliebiger Inhalt) ab oder legt sie fest, die über „unbekannte Beziehungen“ mit dem OOXML-Paket verknüpft sind.

```csharp
public CustomPartCollection PackageCustomParts { get; set; }
```

## Bemerkungen

Verwechseln Sie diese benutzerdefinierten Teile nicht mit benutzerdefinierten XML-Daten. Wenn Sie auf benutzerdefinierte XML-Teile zugreifen müssen, verwenden Sie die[`CustomXmlParts`](../customxmlparts/) Eigentum.

Diese Sammlung enthält OOXML-Teile, deren übergeordnetes Element das OOXML-Paket ist und deren Ziele eine „unbekannte Beziehung“ aufweisen. Weitere Informationen finden Sie unter[`CustomPart`](../../../aspose.words.markup/custompart/).

Aspose.Words lädt und speichert benutzerdefinierte Teile nur in OOXML-Dokumenten.

Diese Eigenschaft kann nicht`null`.

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

* class [CustomPartCollection](../../../aspose.words.markup/custompartcollection/)
* class [Document](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
