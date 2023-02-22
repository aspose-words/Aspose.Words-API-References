---
title: Class FieldEmbed
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldEmbed klass. Implementerar fältet EMBED.
type: docs
weight: 1700
url: /sv/net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

Implementerar fältet EMBED.

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
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Exempel

Visar hur vissa äldre Microsoft Word-fält som SHAPE och EMBED hanteras under laddning.

```csharp
// Öppna ett dokument som skapades i Microsoft Word 2003.
Document doc = new Document(MyDir + "Legacy fields.doc");

// Om vi öppnar Word-dokumentet och trycker på Alt+F9 kommer vi att se ett SHAPE- och ett EMBED-fält.
// Ett SHAPE-fält är ankare/canvas för ett AutoShape-objekt med inslagsstilen "I linje med text" aktiverad.
// Ett EMBED-fält har samma funktion, men för ett inbäddat objekt,
// som ett kalkylblad från ett externt Excel-dokument.
// Dessa fält kommer dock inte att visas i dokumentets fältsamling.
Assert.AreEqual(0, doc.Range.Fields.Count);

// Dessa fält stöds endast av gamla versioner av Microsoft Word.
// Dokumentladdningsprocessen kommer att konvertera dessa fält till Shape-objekt,
// som vi kan komma åt i dokumentets nodsamling.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// Den första Shape-noden motsvarar fältet SHAPE i inmatningsdokumentet,
// som är inline-duken för AutoShape.
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// Den andra Shape-noden är själva AutoShape.
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// Den tredje Shape är det som var EMBED-fältet som innehöll det externa kalkylarket.
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


