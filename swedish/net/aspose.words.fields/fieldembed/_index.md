---
title: FieldEmbed Class
linktitle: FieldEmbed
articleTitle: FieldEmbed
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldEmbed för sömlös implementering av EMBED-fält, vilket förbättrar dokumentfunktionalitet och mångsidighet.
type: docs
weight: 2260
url: /sv/net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

Implementerar EMBED-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldEmbed : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldEmbed](fieldembed/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Exempel

Visar hur vissa äldre Microsoft Word-fält, som SHAPE och EMBED, hanteras under inläsning.

```csharp
// Öppna ett dokument som skapades i Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Om vi öppnar Word-dokumentet och trycker Alt+F9, ser vi en SHAPE och ett EMBED-fält.
// Ett SHAPE-fält är ankaret/arbetsytan för ett AutoShape-objekt med radbrytningsstilen "I linje med text" aktiverad.
// Ett EMBED-fält har samma funktion, men för ett inbäddat objekt,
// som till exempel ett kalkylblad från ett externt Excel-dokument.
// Dessa fält kommer dock inte att visas i dokumentets Fields-samling.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Dessa fält stöds endast av äldre versioner av Microsoft Word.
// Dokumentinläsningsprocessen konverterar dessa fält till formobjekt,
// som vi kan komma åt i dokumentets nodsamling.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Den första Shape-noden motsvarar SHAPE-fältet i indatadokumentet,
// vilket är den inbäddade arbetsytan för autoformen.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Den andra formnoden är själva autoformen.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Den tredje formen är det som var EMBED-fältet som innehöll det externa kalkylbladet.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
