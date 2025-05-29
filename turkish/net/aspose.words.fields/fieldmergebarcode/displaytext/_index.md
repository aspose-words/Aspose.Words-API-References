---
title: FieldMergeBarcode.DisplayText
linktitle: DisplayText
articleTitle: DisplayText
second_title: .NET için Aspose.Words
description: FieldMergeBarcode'un DisplayText özelliği ile barkod metin gösterimini kontrol edin. Uygulamalarınızdaki okunabilirliği ve işlevselliği zahmetsizce geliştirin.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldmergebarcode/displaytext/
---
## FieldMergeBarcode.DisplayText property

Barkod verilerinin (metin) görüntüyle birlikte görüntülenip görüntülenmeyeceğini alır veya ayarlar.

```csharp
public bool DisplayText { get; set; }
```

## Örnekler

EAN13 barkodlarında posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Posta birleştirme sırasında bir veri kaynağından değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, birleştirme veri kaynağının "MyEAN13Barcode" sütunundaki tüm değerleri EAN13 barkodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "EAN13";
field.BarcodeValue = "MyEAN13Barcode";

// Çubukların altında barkodun sayısal değerini göster.
field.DisplayText = true;
field.PosCodeStyle = "CASE";
field.FixCheckDigit = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyEAN13Barcode EAN13 \\t \\p CASE \\x", field.GetFieldCode());
builder.Writeln();

// MERGEBARCODE alanımızın BarcodeValue'su ile aynı adı taşıyan bir sütuna sahip bir DataTable oluşturun.
// Posta birleştirme her satır için yeni bir sayfa oluşturacaktır. Her sayfa bir DISPLAYBARCODE alanı içerecektir.
// Birleştirilmiş satırdaki değerle bir EAN13 barkodu görüntülenecektir.
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
