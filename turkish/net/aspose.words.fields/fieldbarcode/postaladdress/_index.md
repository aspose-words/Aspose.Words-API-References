---
title: FieldBarcode.PostalAddress
second_title: Aspose.Words for .NET API Referansı
description: FieldBarcode mülk. Barkod oluşturmak için kullanılan posta adresini veya ona başvuran yer iminin adını alır veya ayarlar.
type: docs
weight: 50
url: /tr/net/aspose.words.fields/fieldbarcode/postaladdress/
---
## FieldBarcode.PostalAddress property

Barkod oluşturmak için kullanılan posta adresini veya ona başvuran yer iminin adını alır veya ayarlar.

```csharp
public string PostalAddress { get; set; }
```

### Örnekler

ABD Posta kodlarını barkod biçiminde görüntülemek için BARKOD alanının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// Aşağıda, özel değerleri barkod olarak görüntülemek için BARKOD alanlarını kullanmanın iki yolu bulunmaktadır.
// 1 - Barkodun göstereceği değeri PostalAddress özelliğinde saklayın:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// Bu değerin geçerli bir posta kodu olması gerekiyor.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - Bu barkodun göstereceği değeri depolayan bir yer işaretine başvurun:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// BARKOD alanının PostalAddress özelliğinde başvurduğu yer imi
// geçerli ZIP kodu dışında hiçbir şey içermemelidir.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### Ayrıca bakınız

* class [FieldBarcode](../)
* ad alanı [Aspose.Words.Fields](../../fieldbarcode/)
* toplantı [Aspose.Words](../../../)


