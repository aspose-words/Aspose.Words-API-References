---
title: FieldMergeBarcode.AddStartStopChar
linktitle: AddStartStopChar
articleTitle: AddStartStopChar
second_title: .NET için Aspose.Words
description: FieldMergeBarcode AddStartStopChar özelliğiyle NW7 ve CODE39 barkodları için Başlat/Durdur karakterlerini kontrol edin. Barkod işlevselliğinizi bugün geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldmergebarcode/addstartstopchar/
---
## FieldMergeBarcode.AddStartStopChar property

Barkod türleri NW7 ve CODE39 için Başlangıç/Durdurma karakterlerinin eklenip eklenmeyeceğini alır veya ayarlar.

```csharp
public bool AddStartStopChar { get; set; }
```

## Örnekler

CODE39 barkodlarında posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Posta birleştirme sırasında bir veri kaynağından değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, birleştirme veri kaynağının "MyCODE39Barcode" sütunundaki tüm değerleri CODE39 barkodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Başlangıç/bitiş karakterlerini görüntülemek için görünümünü düzenleyin.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// MERGEBARCODE alanımızın BarcodeValue'su ile aynı adı taşıyan bir sütuna sahip bir DataTable oluşturun.
// Posta birleştirme her satır için yeni bir sayfa oluşturacaktır. Her sayfa bir DISPLAYBARCODE alanı içerecektir.
// birleştirilmiş satırdaki değerle bir CODE39 barkodu görüntülenecektir.
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

### Ayrıca bakınız

* class [FieldMergeBarcode](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
