---
title: FieldPrintDate
second_title: Aspose.Words för .NET API Referens
description: Implementerar fältet PRINTDATE.
type: docs
weight: 2140
url: /sv/net/aspose.words.fields/fieldprintdate/
---
## FieldPrintDate class

Implementerar fältet PRINTDATE.

```csharp
public class FieldPrintDate : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldPrintDate](fieldprintdate)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format) { get; } | Får en[`FieldFormat`](../fieldformat) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Hämtar fälttypen Microsoft Word. |
| [UseLunarCalendar](../../aspose.words.fields/fieldprintdate/uselunarcalendar) { get; set; } | Hämtar eller ställer in om du vill använda Hijri Lunar eller Hebrew Lunar kalender. |
| [UseSakaEraCalendar](../../aspose.words.fields/fieldprintdate/usesakaeracalendar) { get; set; } | Hämtar eller ställer in om Saka Era-kalendern ska användas. |
| [UseUmAlQuraCalendar](../../aspose.words.fields/fieldprintdate/useumalquracalendar) { get; set; } | Hämtar eller ställer in om Um-al-Qura-kalendern ska användas. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Hämtar datum och tid då dokumentet senast skrevs ut. Som standard används den gregorianska kalendern.

### Exempel

Visar läs PRINTDATE-fält.

```csharp
Document doc = new Document(MyDir + "Field sample - PRINTDATE.docx");

// När ett dokument skrivs ut av en skrivare eller skrivs ut som en PDF (men inte exporteras till PDF),
// PRINTDATE-fälten visar utskriftsoperationens datum/tid.
// Om ingen utskrift har skett kommer dessa fält att visa "0/0/0000".
FieldPrintDate field = (FieldPrintDate)doc.Range.Fields[0];

Assert.AreEqual("3/25/2020 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE ", field.GetFieldCode());

// Nedan finns tre olika kalendertyper enligt vilka PRINTDATE-fältet
// kan visa datum och tid för den senaste utskriften.
// 1 - Islamisk månkalender:
field = (FieldPrintDate)doc.Range.Fields[1];

Assert.True(field.UseLunarCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\h", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[2];

// 2 - Umm al-Qura kalender:
Assert.True(field.UseUmAlQuraCalendar);
Assert.AreEqual("8/1/1441 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\u", field.GetFieldCode());

field = (FieldPrintDate)doc.Range.Fields[3];

// 3 - Indian National Calendar:
Assert.True(field.UseSakaEraCalendar);
Assert.AreEqual("1/5/1942 12:00:00 AM", field.Result);
Assert.AreEqual(" PRINTDATE  \\s", field.GetFieldCode());
```

### Se även

* class [Field](../field)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
