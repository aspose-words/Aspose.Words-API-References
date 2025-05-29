---
title: CustomPart Class
linktitle: CustomPart
articleTitle: CustomPart
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Markup.CustomPart för flexibel innehållshantering. Skapa enkelt unika, icke-standardiserade delar utöver ISO/IEC 29500!
type: docs
weight: 4590
url: /sv/net/aspose.words.markup/custompart/
---
## CustomPart class

Representerar en anpassad (godtyckligt innehåll) del som inte definieras av ISO/IEC 29500-standarden.

För att lära dig mer, besök[Strukturerade dokumenttaggar eller innehållskontroll](https://docs.aspose.com/words/net/working-with-content-control-sdt/) dokumentationsartikel.

```csharp
public class CustomPart
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [CustomPart](custompart/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ContentType](../../aspose.words.markup/custompart/contenttype/) { get; set; } | Anger innehållstypen för denna anpassade del. |
| [Data](../../aspose.words.markup/custompart/data/) { get; set; } | Innehåller data för denna anpassade del. |
| [IsExternal](../../aspose.words.markup/custompart/isexternal/) { get; set; } | Falskt om denna anpassade del lagras inuti OOXML-paketet. Sant om denna anpassade del är ett externt mål. |
| [Name](../../aspose.words.markup/custompart/name/) { get; set; } | Hämtar eller anger den här delens absoluta namn i OOXML-paketet eller mål-URL:en. |
| [RelationshipType](../../aspose.words.markup/custompart/relationshiptype/) { get; set; } | Hämtar eller anger relationstypen från förälderdelen till denna anpassade del. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.markup/custompart/clone/)() | Skapar en "tillräckligt djup" kopia av objektet. Duplicerar inte byten för[`Data`](./data/) värde. |

## Anmärkningar

Denna klass representerar en OOXML-del som är ett mål för en "okänd relation". Alla relationer som inte definieras inom ISO/IEC 29500 betraktas som "okända relationer". Okända relationer är tillåtna i ett Office Open XML-dokument förutsatt att de följer riktlinjerna för relationsmärkning.

Microsoft Word bevarar anpassade delar under öppnings-/sparacykler. Ytterligare information finns här http://blogs.msdn.com/dmahugh/archive/2006/11/25/arbitrary-content-in-an-opc-package.aspx

Aspose.Words returnerar även anpassade delar och tillåter dessutom programmatisk åtkomst till sådana delar via .`CustomPart` och[`CustomPartCollection`](../custompartcollection/) föremål.

Förväxla inte anpassade delar med anpassade XML-data.[`CustomXmlPart`](../customxmlpart/) om du behöver för att komma åt anpassade XML-data.

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

* namnutrymme [Aspose.Words.Markup](../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../)
