---
title: FieldBarcode.FacingIdentificationMark
linktitle: FacingIdentificationMark
articleTitle: FacingIdentificationMark
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldBarcode FacingIdentificationMark-Eigenschaft, um Facing Identification Marks (FIM) einfach zu verwalten und anzupassen und so die Scaneffizienz zu verbessern.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldbarcode/facingidentificationmark/
---
## FieldBarcode.FacingIdentificationMark property

Ruft den Typ einer einzufügenden Facing Identification Mark (FIM) ab oder legt ihn fest.

```csharp
public string FacingIdentificationMark { get; set; }
```

## Beispiele

Zeigt, wie das BARCODE-Feld verwendet wird, um US-Postleitzahlen in Form eines Barcodes anzuzeigen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Unten sind zwei Möglichkeiten zur Verwendung von BARCODE-Feldern aufgeführt, um benutzerdefinierte Werte als Barcodes anzuzeigen.
// 1 – Speichern Sie den Wert, der im Barcode angezeigt wird, in der Eigenschaft „PostalAddress“:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Dieser Wert muss eine gültige Postleitzahl sein.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 – Verweisen Sie auf ein Lesezeichen, das den Wert speichert, der von diesem Barcode angezeigt wird:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// Das Lesezeichen, auf das das Feld BARCODE in seiner Eigenschaft PostalAddress verweist
// darf außer der gültigen Postleitzahl nichts enthalten.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Siehe auch

* class [FieldBarcode](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
