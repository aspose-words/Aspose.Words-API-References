---
title: CustomPart Class
linktitle: CustomPart
articleTitle: CustomPart
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Markup.CustomPart für flexibles Content-Management. Erstellen Sie mühelos einzigartige, nicht standardisierte Teile, die über ISO/IEC 29500 hinausgehen!
type: docs
weight: 4590
url: /de/net/aspose.words.markup/custompart/
---
## CustomPart class

Stellt einen benutzerdefinierten Teil (mit beliebigem Inhalt) dar, der nicht durch den ISO/IEC 29500-Standard definiert ist.

Um mehr zu erfahren, besuchen Sie die[Strukturierte Dokument-Tags oder Inhaltssteuerung](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Dokumentationsartikel.

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
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | Falsch, wenn dieser benutzerdefinierte Teil im OOXML-Paket gespeichert ist. Wahr, wenn dieser benutzerdefinierte Teil ein externes Ziel ist. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Ruft den absoluten Namen dieses Teils innerhalb des OOXML-Pakets oder der Ziel-URL ab oder legt ihn fest. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Ruft den Beziehungstyp vom übergeordneten Teil zu diesem benutzerdefinierten Teil ab oder legt ihn fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Erstellt eine ausreichend tiefe Kopie des Objekts. Dupliziert nicht die Bytes des[`Data`](./data/) Wert. |

## Bemerkungen

Diese Klasse stellt einen OOXML-Teil dar, der Ziel einer „unbekannten Beziehung“ ist. Alle Beziehungen, die nicht in ISO/IEC 29500 definiert sind, werden als „unbekannte Beziehungen“ betrachtet. Unbekannte Beziehungen sind in einem Office Open XML-Dokument zulässig, sofern sie den Richtlinien zur Beziehungsmarkierung entsprechen.

Microsoft Word behält benutzerdefinierte Teile während des Öffnens/Speicherns bei. Weitere Informationen finden Sie hier: http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words führt auch Roundtrips für benutzerdefinierte Teile durch und ermöglicht darüber hinaus den programmgesteuerten Zugriff auf solche Teile über die`CustomPart` Und[`CustomPartCollection`](../custompartcollection/) Objekte.

Verwechseln Sie benutzerdefinierte Teile nicht mit benutzerdefinierten XML-Daten. Verwenden Sie[`CustomXmlPart`](../customxmlpart/) wenn Sie benötigen, um auf benutzerdefinierte XML-Daten zuzugreifen.

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

* namensraum [Aspose.Words.Markup](../../aspose.words.markup/)
* Montage [Aspose.Words](../../)
