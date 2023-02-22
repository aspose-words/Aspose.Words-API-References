---
title: FieldMergeBarcode.SymbolRotation
second_title: Aspose.Words for .NET API Referansı
description: FieldMergeBarcode mülk. Barkod sembolünün dönüşünü alır veya ayarlar. Geçerli değerler 0 3
type: docs
weight: 140
url: /tr/net/aspose.words.fields/fieldmergebarcode/symbolrotation/
---
## FieldMergeBarcode.SymbolRotation property

Barkod sembolünün dönüşünü alır veya ayarlar. Geçerli değerler: [0, 3]

```csharp
public string SymbolRotation { get; set; }
```

### Örnekler

QR barkodlarında adres mektup birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres mektup birleştirme sırasında bir veri kaynağından değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, bir birleştirme veri kaynağının "MyQRCode" sütunundaki tüm değerleri QR kodlarına dönüştürür.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Özel renkler ve ölçekleme uygula.
field.BackgroundColor = "0xF8BD69";
field.ForegroundColor = "0xB5413B";
field.ErrorCorrectionLevel = "3";
field.ScalingFactor = "250";
field.SymbolHeight = "1000";
field.SymbolRotation = "0";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyQRCode QR \\b 0xF8BD69 \\f 0xB5413B \\q 3 \\s 250 \\h 1000 \\r 0",
    field.GetFieldCode());
builder.Writeln();

// MERGEBARCODE alanımızın BarcodeValue ile aynı ada sahip bir sütunu olan bir DataTable oluşturun.
// Adres mektup birleştirme, her satır için yeni bir sayfa oluşturacaktır. Her sayfa bir EKRAN BARKOD alanı içerecektir,
// birleştirilmiş satırdaki değere sahip bir QR kodu gösterecek.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyQRCode");
table.Rows.Add(new[] { "ABC123" });
table.Rows.Add(new[] { "DEF456" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"ABC123\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B", 
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"DEF456\" QR \\q 3 \\s 250 \\h 1000 \\r 0 \\b 0xF8BD69 \\f 0xB5413B",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.QR.docx");
```

### Ayrıca bakınız

* class [FieldMergeBarcode](../)
* ad alanı [Aspose.Words.Fields](../../fieldmergebarcode/)
* toplantı [Aspose.Words](../../../)


