---
title: Class CustomPart
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Markup.CustomPart klas. Stellt einen benutzerdefinierten Teil beliebiger Inhalt dar der nicht durch den ISO/IEC 29500Standard definiert ist.
type: docs
weight: 3660
url: /de/net/aspose.words.markup/custompart/
---
## CustomPart class

Stellt einen benutzerdefinierten Teil (beliebiger Inhalt) dar, der nicht durch den ISO/IEC 29500-Standard definiert ist.

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
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | `FALSCH` wenn dieser benutzerdefinierte Teil im OOXML-Paket gespeichert ist.`WAHR` wenn dieses benutzerdefinierte Teil ein externes Ziel ist. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Ruft den absoluten Namen dieses Teils innerhalb des OOXML-Pakets oder der Ziel-URL ab oder setzt ihn. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Ruft den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil ab oder legt ihn fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Erstellt eine ausreichend tiefe Kopie des Objekts. Dupliziert die Bytes der nicht[`Data`](./data/) wert. |

### Bemerkungen

Diese Klasse stellt einen OOXML-Teil dar, der Ziel einer „unbekannten Beziehung“ ist. Alle Beziehungen, die nicht in ISO/IEC 29500 definiert sind, gelten als „unbekannte Beziehungen“. Unbekannte Beziehungen sind innerhalb eines Office Open XML-Dokuments zulässig, sofern sie -konform sind zu den Markup-Richtlinien für Beziehungen.

Microsoft Word behält benutzerdefinierte Teile während des Öffnens/Speicherns bei. Einige zusätzliche Informationen finden Sie hier http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words rundet auch benutzerdefinierte Teile ab und ermöglicht zusätzlich den programmgesteuerten Zugriff auf solche Teile über die`CustomPart` und[`CustomPartCollection`](../custompartcollection/) Objekte.

Verwechseln Sie benutzerdefinierte Teile nicht mit benutzerdefinierten XML-Daten. Verwenden[`CustomXmlPart`](../customxmlpart/) wenn Sie benötigen, um auf benutzerdefinierte XML-Daten zuzugreifen.

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)


