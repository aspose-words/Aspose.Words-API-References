---
title: FieldMergeBarcode.PosCodeStyle
linktitle: PosCodeStyle
articleTitle: PosCodeStyle
second_title: Aspose.Words for .NET
description: FieldMergeBarcode PosCodeStyle mülk. Satış Noktası barkodunun stilini alır veya ayarlar barkod türleri UPCAUPCEEAN13EAN8. Geçerli değerler büyük/küçük harfe duyarlı değil şunlardır STDSUP2SUP5CASE C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.fields/fieldmergebarcode/poscodestyle/
---
## FieldMergeBarcode.PosCodeStyle property

Satış Noktası barkodunun stilini alır veya ayarlar (barkod türleri UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Geçerli değerler (büyük/küçük harfe duyarlı değil) şunlardır: [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE].

```csharp
public string PosCodeStyle { get; set; }
```

## Örnekler

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

### Ayrıca bakınız

* class [FieldMergeBarcode](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
