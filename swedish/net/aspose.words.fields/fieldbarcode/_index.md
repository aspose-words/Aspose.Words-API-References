---
title: FieldBarcode Class
linktitle: FieldBarcode
articleTitle: FieldBarcode
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldBarcode för enkel streckkodsgenerering i dokument. Förbättra ditt arbetsflöde med sömlös integration och kraftfulla funktioner.
type: docs
weight: 2040
url: /sv/net/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class

Implementerar streckkodsfältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldBarcode : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldBarcode](fieldbarcode/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [FacingIdentificationMark](../../aspose.words.fields/fieldbarcode/facingidentificationmark/) { get; set; } | Hämtar eller anger typen av ett Facing Identification Mark (FIM) som ska infogas. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsBookmark](../../aspose.words.fields/fieldbarcode/isbookmark/) { get; set; } | Hämtar eller anger om[`PostalAddress`](./postaladdress/) är namnet på ett bokmärke. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [IsUSPostalAddress](../../aspose.words.fields/fieldbarcode/isuspostaladdress/) { get; set; } | Hämtar eller anger om[`PostalAddress`](./postaladdress/) är en amerikansk postadress. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [PostalAddress](../../aspose.words.fields/fieldbarcode/postaladdress/) { get; set; } | Hämtar eller ställer in postadressen som används för att generera en streckkod eller namnet på bokmärket som refererar till den. |
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

Infogar en poststreckkod i en maskinläsbar adressform som används av US Postal Service.

## Exempel

Visar hur man använder fältet STRECKKOD för att visa amerikanska postnummer i form av en streckkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Nedan följer två sätt att använda STRECKKOD-fält för att visa anpassade värden som streckkoder.
// 1 - Lagra värdet som streckkoden ska visa i egenskapen PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Detta värde måste vara ett giltigt postnummer.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Referera till ett bokmärke som lagrar värdet som streckkoden kommer att visa:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Bokmärket som STRECKKOD-fältet refererar till i sin PostalAddress-egenskap
// behöver inte innehålla något annat än det giltiga postnumret.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
