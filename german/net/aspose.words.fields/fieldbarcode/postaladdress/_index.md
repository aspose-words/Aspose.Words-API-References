---
title: FieldBarcode.PostalAddress
linktitle: PostalAddress
articleTitle: PostalAddress
second_title: Aspose.Words für .NET
description: Entdecken Sie die FieldBarcode PostalAddress-Eigenschaft zur einfachen Verwaltung von Postadressen für die Barcode-Generierung und Lesezeichenverweise. Vereinfachen Sie Ihren Workflow noch heute!
type: docs
weight: 50
url: /de/net/aspose.words.fields/fieldbarcode/postaladdress/
---
## FieldBarcode.PostalAddress property

Ruft die zum Generieren eines Barcodes verwendete Postanschrift oder den Namen des Lesezeichens ab, das darauf verweist, oder legt diese fest.

```csharp
public string PostalAddress { get; set; }
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
