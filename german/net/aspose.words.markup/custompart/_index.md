---
title: CustomPart Class
linktitle: CustomPart
articleTitle: CustomPart
second_title: Aspose.Words für .NET
description: Aspose.Words.Markup.CustomPart klas. Stellt einen benutzerdefinierten Teil beliebiger Inhalt dar der nicht durch den ISO/IEC 29500Standard definiert ist in C#.
type: docs
weight: 3900
url: /de/net/aspose.words.markup/custompart/
---
## CustomPart class

Stellt einen benutzerdefinierten Teil (beliebiger Inhalt) dar, der nicht durch den ISO/IEC 29500-Standard definiert ist.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltskontrolle](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

```csharp
public class CustomPart
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [CustomPart](custompart/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | Gibt den Inhaltstyp dieses benutzerdefinierten Teils an. |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | Enthält die Daten dieses benutzerdefinierten Teils. |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | False, wenn dieser benutzerdefinierte Teil im OOXML-Paket gespeichert ist. True, wenn dieses benutzerdefinierte Teil ein externes Ziel ist. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Ruft den absoluten Namen dieses Teils innerhalb des OOXML-Pakets oder der Ziel-URL ab oder legt diesen fest. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Ruft den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil ab oder legt diesen fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Erstellt eine ausreichend tiefe Kopie des Objekts. Dupliziert nicht die Bytes von[`Data`](./data/) value. |

## Bemerkungen

Diese Klasse stellt einen OOXML-Teil dar, der ein Ziel einer „unbekannten Beziehung“ ist. Alle Beziehungen, die nicht in ISO/IEC 29500 definiert sind, gelten als „unbekannte Beziehungen“. Unbekannte Beziehungen sind innerhalb eines Office Open XML-Dokuments zulässig, sofern sie konform sind zu den Beziehungsmarkup-Richtlinien.

Microsoft Word behält benutzerdefinierte Teile während der Öffnungs-/Speicherzyklen bei. Einige zusätzliche Informationen finden Sie hier http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words führt auch Roundtrips benutzerdefinierter Teile durch und ermöglicht darüber hinaus den programmgesteuerten Zugriff auf solcher Teile über`CustomPart` Und[`CustomPartCollection`](../custompartcollection/) Objekte.

Verwechseln Sie benutzerdefinierte Teile nicht mit benutzerdefinierten XML-Daten. Verwenden[`CustomXmlPart`](../customxmlpart/) wenn Sie benötigen, um auf benutzerdefinierte XML-Daten zuzugreifen.

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
