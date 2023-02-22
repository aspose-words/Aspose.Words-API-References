---
title: Class FieldBarcode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldBarcode klass. Implementerar fältet BARCODE.
type: docs
weight: 1480
url: /sv/net/aspose.words.fields/fieldbarcode/
---
## FieldBarcode class

Implementerar fältet BARCODE.

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
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [FacingIdentificationMark](../../aspose.words.fields/fieldbarcode/facingidentificationmark/) { get; set; } | Hämtar eller ställer in typen av ett Facing Identification Mark (FIM) som ska infogas. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsBookmark](../../aspose.words.fields/fieldbarcode/isbookmark/) { get; set; } | Hämtar eller ställer in om[`PostalAddress`](./postaladdress/) är namnet på ett bokmärke. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [IsUSPostalAddress](../../aspose.words.fields/fieldbarcode/isuspostaladdress/) { get; set; } | Hämtar eller ställer in om[`PostalAddress`](./postaladdress/) är en amerikansk postadress. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [PostalAddress](../../aspose.words.fields/fieldbarcode/postaladdress/) { get; set; } | Hämtar eller ställer in postadressen som används för att generera en streckkod eller namnet på bokmärket som refererar till den. |
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

### Anmärkningar

Infogar en poststreckkod i en maskinläsbar adressform som används av US Postal Service.

### Exempel

Visar hur man använder streckkodsfältet för att visa amerikanska postnummer i form av en streckkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Nedan finns två sätt att använda STreckkodsfält för att visa anpassade värden som streckkoder.
// 1 - Lagra värdet som streckkoden kommer att visa i egenskapen PostalAddress:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Detta värde måste vara ett giltigt postnummer.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Referera till ett bokmärke som lagrar värdet som denna streckkod kommer att visa:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Bokmärket som BARCODE-fältet refererar till i sin PostalAddress-egenskap
// behöver inte innehålla något förutom det giltiga postnumret.
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


