---
title: FieldMergeBarcode Class
linktitle: FieldMergeBarcode
articleTitle: FieldMergeBarcode
second_title: .NET için Aspose.Words
description: Gelişmiş belge otomasyonu ve verimliliği için MERGEBARCODE alanlarını zahmetsizce uygulamak üzere Aspose.Words.Fields.FieldMergeBarcode sınıfını keşfedin.
type: docs
weight: 2550
url: /tr/net/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class

MERGEBARCODE alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class FieldMergeBarcode : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldMergeBarcode](fieldmergebarcode/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AddStartStopChar](../../aspose.words.fields/fieldmergebarcode/addstartstopchar/) { get; set; } | Barkod türleri NW7 ve CODE39 için Başlangıç/Durdurma karakterlerinin eklenip eklenmeyeceğini alır veya ayarlar. |
| [BackgroundColor](../../aspose.words.fields/fieldmergebarcode/backgroundcolor/) { get; set; } | Barkod sembolünün arka plan rengini alır veya ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır |
| [BarcodeType](../../aspose.words.fields/fieldmergebarcode/barcodetype/) { get; set; } | Barkod türünü (QR, vb.) alır veya ayarlar |
| [BarcodeValue](../../aspose.words.fields/fieldmergebarcode/barcodevalue/) { get; set; } | Barkod değerini alır veya ayarlar. |
| [CaseCodeStyle](../../aspose.words.fields/fieldmergebarcode/casecodestyle/) { get; set; } | Barkod türü ITF14 için bir Durum Kodunun stilini alır veya ayarlar. Geçerli değerler şunlardır [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [DisplayText](../../aspose.words.fields/fieldmergebarcode/displaytext/) { get; set; } | Barkod verilerinin (metin) görüntüyle birlikte görüntülenip görüntülenmeyeceğini alır veya ayarlar. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fieldmergebarcode/errorcorrectionlevel/) { get; set; } | QR Kodunun hata düzeltme düzeyini alır veya ayarlar. Geçerli değerler [0, 3]'tür. |
| [FixCheckDigit](../../aspose.words.fields/fieldmergebarcode/fixcheckdigit/) { get; set; } | Kontrol basamağının geçersiz olması durumunda düzeltilip düzeltilmeyeceğini alır veya ayarlar. |
| [ForegroundColor](../../aspose.words.fields/fieldmergebarcode/foregroundcolor/) { get; set; } | Barkod sembolünün ön plan rengini alır veya ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PosCodeStyle](../../aspose.words.fields/fieldmergebarcode/poscodestyle/) { get; set; } | Bir Satış Noktası barkodunun stilini alır veya ayarlar (barkod türleri UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Geçerli değerler (büyük/küçük harfe duyarlı değildir) [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [ScalingFactor](../../aspose.words.fields/fieldmergebarcode/scalingfactor/) { get; set; } | Sembol için bir ölçekleme faktörü alır veya ayarlar. Değer tam yüzde puan cinsindendir ve geçerli değerler [10, 1000]'dir |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [SymbolHeight](../../aspose.words.fields/fieldmergebarcode/symbolheight/) { get; set; } | Sembolün yüksekliğini alır veya ayarlar. Birimler TWIPS (1/1440 inç) cinsindendir. |
| [SymbolRotation](../../aspose.words.fields/fieldmergebarcode/symbolrotation/) { get; set; } | Barkod sembolünün dönüşünü alır veya ayarlar. Geçerli değerler [0, 3]'tür |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Hem alan kodu hem de alt alanların alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcısı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son alt 'siyse, üst paragrafını döndürür. Alan zaten kaldırılmışsa, şunu döndürür`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alan bağlantısını kaldırma işlemini gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa fırlatır. |

## Notlar

Barkod birleştirme.

## Örnekler

ITF14 barkodlarında posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Posta birleştirme sırasında bir veri kaynağından değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, birleştirme veri kaynağının "MyITF14Barcode" sütunundaki tüm değerleri ITF14 barkodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// MERGEBARCODE alanımızın BarcodeValue'su ile aynı adı taşıyan bir sütuna sahip bir DataTable oluşturun.
// Posta birleştirme her satır için yeni bir sayfa oluşturacaktır. Her sayfa bir DISPLAYBARCODE alanı içerecektir.
// Birleştirilmiş satırdaki değerle bir ITF14 barkodu görüntülenecektir.
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

QR barkodlarında posta birleştirme işleminin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Posta birleştirme sırasında bir veri kaynağından değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, birleştirme veri kaynağının "MyQRCode" sütunundaki tüm değerleri QR kodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "QR";
field.BarcodeValue = "MyQRCode";

// Özel renkler ve ölçekleme uygulayın.
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

// MERGEBARCODE alanımızın BarcodeValue'su ile aynı adı taşıyan bir sütuna sahip bir DataTable oluşturun.
// Posta birleştirme her satır için yeni bir sayfa oluşturacaktır. Her sayfa bir DISPLAYBARCODE alanı içerecektir.
// Birleştirilmiş satırdaki değerin yer aldığı bir QR kodu görüntülenecektir.
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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
