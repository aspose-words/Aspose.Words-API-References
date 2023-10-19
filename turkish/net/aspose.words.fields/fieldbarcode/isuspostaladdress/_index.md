---
title: FieldBarcode.IsUSPostalAddress
linktitle: IsUSPostalAddress
articleTitle: IsUSPostalAddress
second_title: Aspose.Words for .NET
description: FieldBarcode IsUSPostalAddress mülk. Alır veya ayarlarPostalAddress ABD posta adresidir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldbarcode/isuspostaladdress/
---
## FieldBarcode.IsUSPostalAddress property

Alır veya ayarlar[`PostalAddress`](../postaladdress/) ABD posta adresidir.

```csharp
public bool IsUSPostalAddress { get; set; }
```

## Örnekler

ABD Posta kodlarını barkod biçiminde görüntülemek için BARKOD alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Aşağıda özel değerleri barkod olarak görüntülemek için BARCODE alanlarını kullanmanın iki yolu verilmiştir.
// 1 - Barkodun görüntüleyeceği değeri PostalAddress özelliğinde saklayın:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Bu değerin geçerli bir posta kodu olması gerekiyor.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Bu barkodun görüntüleyeceği değeri saklayan bir yer imine referans verin:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// BARCODE alanının PostalAddress özelliğinde başvurduğu yer işareti
// geçerli posta kodu dışında hiçbir şey içermemelidir.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Ayrıca bakınız

* class [FieldBarcode](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
