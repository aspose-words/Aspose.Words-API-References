---
title: FieldMergeBarcode.BarcodeType
linktitle: BarcodeType
articleTitle: BarcodeType
second_title: Aspose.Words for .NET
description: FieldMergeBarcode BarcodeType mülk. Barkod türünü QR vb. alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldmergebarcode/barcodetype/
---
## FieldMergeBarcode.BarcodeType property

Barkod türünü (QR vb.) alır veya ayarlar.

```csharp
public string BarcodeType { get; set; }
```

## Örnekler

ITF14 barkodlarında adres-mektup birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres-mektup birleştirme sırasında veri kaynağından gelen değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, birleştirme veri kaynağının "MyITF14Barcode" sütunundaki tüm değerleri ITF14 barkodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// MERGEBARCODE alanımızın BarcodeValue değeriyle aynı adı taşıyan bir sütuna sahip bir DataTable oluşturun.
// Adres-mektup birleştirme her satır için yeni bir sayfa oluşturacaktır. Her sayfada bir DISPLAYBARCODE alanı bulunacaktır.
// bu, birleştirilmiş satırdaki değeri içeren bir ITF14 barkodunu görüntüleyecektir.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyITF14Barcode");
table.Rows.Add(new[] { "09312345678907" });
table.Rows.Add(new[] { "1234567891234" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"09312345678907\" ITF14 \\c STD",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"1234567891234\" ITF14 \\c STD",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.ITF14.docx");
```

CODE39 barkodlarında adres-mektup birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres-mektup birleştirme sırasında veri kaynağından gelen değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, birleştirme veri kaynağının "MyCODE39Barcode" sütunundaki tüm değerleri CODE39 barkodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Başlangıç/durdurma karakterlerini görüntülemek için görünümünü düzenleyin.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// MERGEBARCODE alanımızın BarcodeValue değeriyle aynı adı taşıyan bir sütuna sahip bir DataTable oluşturun.
// Adres-mektup birleştirme her satır için yeni bir sayfa oluşturacaktır. Her sayfada bir DISPLAYBARCODE alanı bulunacaktır.
// birleştirilmiş satırdaki değerle birlikte CODE39 barkodunu görüntüleyecektir.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyCODE39Barcode");
table.Rows.Add(new[] { "12345ABCDE" });
table.Rows.Add(new[] { "67890FGHIJ" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"12345ABCDE\" CODE39 \\d",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"67890FGHIJ\" CODE39 \\d",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.CODE39.docx");
```

EAN13 barkodlarında adres-mektup birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres-mektup birleştirme sırasında veri kaynağından gelen değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, birleştirme veri kaynağının "MyEAN13Barcode" sütunundaki tüm değerleri EAN13 barkodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Barkodun sayısal değerini çubukların altında görüntüleyin.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// MERGEBARCODE alanımızın BarcodeValue değeriyle aynı adı taşıyan bir sütuna sahip bir DataTable oluşturun.
// Adres-mektup birleştirme her satır için yeni bir sayfa oluşturacaktır. Her sayfada bir DISPLAYBARCODE alanı bulunacaktır.
// bu, birleştirilmiş satırdaki değerle birlikte bir EAN13 barkodunu görüntüleyecektir.
DataTable table = new DataTable("Barcodes");
table.Columns.Add("MyEAN13Barcode");
table.Rows.Add(new[] { "501234567890" });
table.Rows.Add(new[] { "123456789012" });

doc.MailMerge.Execute(table);

Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[0].Type);
Assert.AreEqual("DISPLAYBARCODE \"501234567890\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(FieldType.FieldDisplayBarcode, doc.Range.Fields[1].Type);
Assert.AreEqual("DISPLAYBARCODE \"123456789012\" EAN13 \\t \\p CASE \\x",
    doc.Range.Fields[1].GetFieldCode());

doc.Save(ArtifactsDir + "Field.MERGEBARCODE.EAN13.docx");
```

QR barkodlarında adres-mektup birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres-mektup birleştirme sırasında veri kaynağından gelen değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, birleştirme veri kaynağının "MyQRCode" sütunundaki tüm değerleri QR kodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Özel renkler ve ölçeklendirme uygulayın.
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

// MERGEBARCODE alanımızın BarcodeValue değeriyle aynı adı taşıyan bir sütuna sahip bir DataTable oluşturun.
// Adres-mektup birleştirme her satır için yeni bir sayfa oluşturacaktır. Her sayfada bir DISPLAYBARCODE alanı bulunacaktır.
// bu, birleştirilmiş satırdaki değeri içeren bir QR kodunu görüntüleyecektir.
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
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
