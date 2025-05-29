---
title: FieldAdvance Class
linktitle: FieldAdvance
articleTitle: FieldAdvance
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldAdvance för sömlös implementering av ADVANCE-fält och förbättra dina dokumentbehandlingsmöjligheter utan ansträngning.
type: docs
weight: 1950
url: /sv/net/aspose.words.fields/fieldadvance/
---
## FieldAdvance class

Implementerar ADVANCE-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldAdvance : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldAdvance](fieldadvance/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [DownOffset](../../aspose.words.fields/fieldadvance/downoffset/) { get; set; } | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas nedåt med. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [HorizontalPosition](../../aspose.words.fields/fieldadvance/horizontalposition/) { get; set; } | Hämtar eller anger antalet punkter med vilka texten som följer fältet ska flyttas horisontellt. från kolumnens, ramens eller textrutans vänstra kant. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LeftOffset](../../aspose.words.fields/fieldadvance/leftoffset/) { get; set; } | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas åt vänster med. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [RightOffset](../../aspose.words.fields/fieldadvance/rightoffset/) { get; set; } | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas åt höger med. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |
| [UpOffset](../../aspose.words.fields/fieldadvance/upoffset/) { get; set; } | Hämtar eller anger antalet punkter som texten som följer fältet ska flyttas uppåt med. |
| [VerticalPosition](../../aspose.words.fields/fieldadvance/verticalposition/) { get; set; } | Hämtar eller anger antalet punkter med vilka texten som följer fältet ska flyttas vertikalt från sidans överkant. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

Flyttar startpunkten där texten som lexiskt följer fältet visas till höger eller vänster, upp eller ner, eller till en specifik horisontell eller vertikal position.

## Exempel

Visar hur man infogar ett ADVANCE-fält och redigerar dess egenskaper.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Nedan följer två sätt att använda fältet ADVANCE för att justera positionen för text som följer det.
// Effekterna av ett ADVANCE-fält fortsätter att tillämpas tills stycket slutar,
// eller ett annat ADVANCE-fält uppdaterar offset-/koordinatvärdena.
// 1 - Ange en riktningsförskjutning:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Flytta text till en position som anges med koordinater:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
