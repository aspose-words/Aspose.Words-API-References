---
title: FieldBarcode.FacingIdentificationMark
linktitle: FacingIdentificationMark
articleTitle: FacingIdentificationMark
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldBarcode FacingIdentificationMark för att enkelt hantera och anpassa Facing Identification Marks (FIM) för förbättrad skanningseffektivitet.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldbarcode/facingidentificationmark/
---
## FieldBarcode.FacingIdentificationMark property

Hämtar eller anger typen av ett Facing Identification Mark (FIM) som ska infogas.

```csharp
public string FacingIdentificationMark { get; set; }
```

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

* class [FieldBarcode](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
