---
title: FieldBarcode.FacingIdentificationMark
linktitle: FacingIdentificationMark
articleTitle: FacingIdentificationMark
second_title: .NET için Aspose.Words
description: Gelişmiş tarama verimliliği için Yüz Tanımlama İşaretlerini (FIM) kolayca yönetmek ve özelleştirmek amacıyla FieldBarcode FacingIdentificationMark özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldbarcode/facingidentificationmark/
---
## FieldBarcode.FacingIdentificationMark property

Eklenecek Yüz Tanımlama İşareti (FIM) türünü alır veya ayarlar.

```csharp
public string FacingIdentificationMark { get; set; }
```

## Örnekler

ABD posta kodlarının barkod biçiminde görüntülenmesi için BARKOD alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Aşağıda BARKOD alanlarını kullanarak özel değerleri barkod olarak görüntülemenin iki yolu bulunmaktadır.
// 1 - Barkodun PostalAddress özelliğinde göstereceği değeri depola:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Bu değerin geçerli bir posta kodu olması gerekiyor.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Bu barkodun göstereceği değeri depolayan bir yer imine başvurun:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// BARCODE alanının PostalAddress özelliğinde başvurduğu yer imi
// geçerli posta kodundan başka hiçbir şey içermemesi gerekiyor.
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
