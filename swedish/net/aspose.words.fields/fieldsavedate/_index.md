---
title: FieldSaveDate Class
linktitle: FieldSaveDate
articleTitle: FieldSaveDate
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldSaveDate, utformad för att enkelt implementera SAVEDATE-fältet för effektiv dokumenthantering.
type: docs
weight: 2760
url: /sv/net/aspose.words.fields/fieldsavedate/
---
## FieldSaveDate class

Implementerar fältet SAVEDATE.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldSaveDate : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldSaveDate](fieldsavedate/)() | Default_Constructor |

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
| [UseLunarCalendar](../../aspose.words.fields/fieldsavedate/uselunarcalendar/) { get; set; } | Hämtar eller anger om Hijri-månkalendern eller den hebreiska månkalendern ska användas. |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldsavedate/usesakaeracalendar/) { get; set; } | Hämtar eller anger om Saka-erans kalender ska användas. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldsavedate/useumalquracalendar/) { get; set; } | Hämtar eller anger om Um-al-Qura-kalendern ska användas. |

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

Hämtar datum och tid då dokumentet senast sparades. Som standard används den gregorianska kalendern.

## Exempel

Visar hur man använder fältet SPARADATUM för att visa datum/tid för dokumentets senaste sparningsåtgärd som utfördes med Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.Writeln(" Date this document was last saved:");

// Vi kan använda fältet SAVEDATE för att visa datum och tid för den senaste sparningen i dokumentet.
// Sparoperationen som dessa fält refererar till är den manuella sparoperationen i ett program som Microsoft Word,
// inte dokumentets Spara-metod.
// Nedan visas tre olika kalendertyper enligt vilka fältet SPARADATUM kan visa datum/tid.
// 1 - Islamisk månkalender:
builder.Write("According to the Lunar Calendar - ");
FieldSaveDate field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseLunarCalendar = true;

Assert.AreEqual(" SAVEDATE  \\h", field.GetFieldCode());

// 2 - Umm al-Qura-kalendern:
builder.Write("\nAccording to the Umm al-Qura calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseUmAlQuraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\u", field.GetFieldCode());

// 3 - Indisk nationalkalender:
builder.Write("\nAccording to the Indian National calendar - ");
field = (FieldSaveDate)builder.InsertField(FieldType.FieldSaveDate, true);
field.UseSakaEraCalendar = true;

Assert.AreEqual(" SAVEDATE  \\s", field.GetFieldCode());

// SAVEDATE-fälten hämtar sina datum-/tidsvärden från den inbyggda egenskapen LastSavedTime.
// Dokumentets Save-metod kommer inte att uppdatera detta värde, men vi kan fortfarande uppdatera det manuellt.
doc.BuiltInDocumentProperties.LastSavedTime = DateTime.Now;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SAVEDATE.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
