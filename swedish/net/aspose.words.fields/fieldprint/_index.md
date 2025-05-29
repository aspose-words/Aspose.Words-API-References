---
title: FieldPrint Class
linktitle: FieldPrint
articleTitle: FieldPrint
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldPrint för sömlös implementering av PRINT-fält. Förbättra din dokumenthantering med kraftfulla funktioner idag!
type: docs
weight: 2690
url: /sv/net/aspose.words.fields/fieldprint/
---
## FieldPrint class

Implementerar PRINT-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldPrint : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldPrint](fieldprint/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [PostScriptGroup](../../aspose.words.fields/fieldprint/postscriptgroup/) { get; set; } | Hämtar eller ställer in ritningsrektangeln som PostScript-instruktionerna fungerar på. |
| [PrinterInstructions](../../aspose.words.fields/fieldprint/printerinstructions/) { get; set; } | Hämtar eller ställer in skrivarspecifika kontrollkodstecken eller PostScript-instruktioner. |
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

## Anmärkningar

En instruktion för att skicka de skrivarspecifika kontrollkodstecknen till den valda skrivaren när dokumentet skrivs ut.

## Exempel

Visar för att infoga ett PRINT-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Fältet PRINT kan skicka instruktioner till skrivaren.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Ange området där skrivaren ska utföra instruktioner.
// I det här fallet kommer det att vara stycket som innehåller vårt PRINT-fält.
field.PostScriptGroup = "para";

// När vi använder en skrivare som stöder PostScript för att skriva ut vårt dokument,
// det här kommandot kommer att göra hela området som vi angav i "field.PostScriptGroup" vitt.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
