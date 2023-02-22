---
title: Class FieldMergeBarcode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldMergeBarcode sınıf. MERGEBARCODE alanını uygular.
type: docs
weight: 1990
url: /tr/net/aspose.words.fields/fieldmergebarcode/
---
## FieldMergeBarcode class

MERGEBARCODE alanını uygular.

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
| [AddStartStopChar](../../aspose.words.fields/fieldmergebarcode/addstartstopchar/) { get; set; } | Barkod türleri NW7 ve CODE39 için Başlat/Durdur karakterlerinin eklenip eklenmeyeceğini alır veya ayarlar. |
| [BackgroundColor](../../aspose.words.fields/fieldmergebarcode/backgroundcolor/) { get; set; } | Barkod sembolünün arka plan rengini alır veya ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır |
| [BarcodeType](../../aspose.words.fields/fieldmergebarcode/barcodetype/) { get; set; } | Barkod türünü (QR, vb.) alır veya ayarlar |
| [BarcodeValue](../../aspose.words.fields/fieldmergebarcode/barcodevalue/) { get; set; } | Barkod değerini alır veya ayarlar. |
| [CaseCodeStyle](../../aspose.words.fields/fieldmergebarcode/casecodestyle/) { get; set; } | Barkod türü ITF14 için Vaka Kodu stilini alır veya ayarlar. Geçerli değerler: [STD&#x7C;EXT&#x7C;ADD] |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [DisplayText](../../aspose.words.fields/fieldmergebarcode/displaytext/) { get; set; } | Resimle birlikte barkod verilerinin (metin) görüntülenip görüntülenmeyeceğini ayarlar veya alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [ErrorCorrectionLevel](../../aspose.words.fields/fieldmergebarcode/errorcorrectionlevel/) { get; set; } | QR Kodunun hata düzeltme düzeyini alır veya ayarlar. Geçerli değerler [0, 3]. |
| [FixCheckDigit](../../aspose.words.fields/fieldmergebarcode/fixcheckdigit/) { get; set; } | Geçersizse kontrol basamağının düzeltilip düzeltilmeyeceğini alır veya ayarlar. |
| [ForegroundColor](../../aspose.words.fields/fieldmergebarcode/foregroundcolor/) { get; set; } | Barkod sembolünün ön plan rengini alır veya ayarlar. Geçerli değerler [0, 0xFFFFFF] aralığındadır |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [PosCodeStyle](../../aspose.words.fields/fieldmergebarcode/poscodestyle/) { get; set; } | Bir Satış Noktası barkodunun stilini alır veya ayarlar (barkod türleri UPCA&#x7C;UPCE&#x7C;EAN13&#x7C;EAN8). Geçerli değerler (büyük/küçük harfe duyarlı değildir) [STD&#x7C;SUP2&#x7C;SUP5&#x7C;CASE]. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [ScalingFactor](../../aspose.words.fields/fieldmergebarcode/scalingfactor/) { get; set; } | Sembol için bir ölçekleme faktörü alır veya ayarlar. Değer tam yüzde puanlarındadır ve geçerli değerler [10, 1000] şeklindedir. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| [SymbolHeight](../../aspose.words.fields/fieldmergebarcode/symbolheight/) { get; set; } | Sembolün yüksekliğini alır veya ayarlar. Birimler TWIPS (1/1440 inç) cinsindendir. |
| [SymbolRotation](../../aspose.words.fields/fieldmergebarcode/symbolrotation/) { get; set; } | Barkod sembolünün dönüşünü alır veya ayarlar. Geçerli değerler: [0, 3] |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alandan hemen sonra bir düğüm döndürür. Alanın sonu, üst düğümünün son çocuğu ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa, döner **hükümsüz** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Bağlantıyı kaldır alanını gerçekleştirir. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

### Notlar

Bir barkodu postayla birleştirme.

### Örnekler

ITF14 barkodlarında adres mektup birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres mektup birleştirme sırasında bir veri kaynağından değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, bir birleştirme veri kaynağının "MyITF14Barcode" sütunundaki tüm değerleri ITF14 barkodlarına dönüştürecektir.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "ITF14";
field.BarcodeValue = "MyITF14Barcode";
field.CaseCodeStyle = "STD";

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyITF14Barcode ITF14 \\c STD", field.GetFieldCode());

// MERGEBARCODE alanımızın BarcodeValue ile aynı ada sahip bir sütunu olan bir DataTable oluşturun.
// Adres mektup birleştirme, her satır için yeni bir sayfa oluşturacaktır. Her sayfa bir EKRAN BARKOD alanı içerecektir,
// birleştirilmiş satırdaki değere sahip bir ITF14 barkodu gösterecek.
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

CODE39 barkodlarında adres mektup birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres mektup birleştirme sırasında bir veri kaynağından değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, bir birleştirme veri kaynağının "MyCODE39Barcode" sütunundaki tüm değerleri CODE39 barkodlarına dönüştürür.
FieldMergeBarcode field = (FieldMergeBarcode)builder.InsertField(FieldType.FieldMergeBarcode, true);
field.BarcodeType = "CODE39";
field.BarcodeValue = "MyCODE39Barcode";

// Başlat/durdur karakterlerini görüntülemek için görünümünü düzenleyin.
field.AddStartStopChar = true;

Assert.AreEqual(FieldType.FieldMergeBarcode, field.Type);
Assert.AreEqual(" MERGEBARCODE  MyCODE39Barcode CODE39 \\d", field.GetFieldCode());
builder.Writeln();

// MERGEBARCODE alanımızın BarcodeValue ile aynı ada sahip bir sütunu olan bir DataTable oluşturun.
// Adres mektup birleştirme, her satır için yeni bir sayfa oluşturacaktır. Her sayfa bir EKRAN BARKOD alanı içerecektir,
// birleştirilmiş satırdaki değerle birlikte bir CODE39 barkodu görüntüleyecektir.
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

EAN13 barkodlarında adres mektup birleştirmenin nasıl gerçekleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adres mektup birleştirme sırasında bir veri kaynağından değerleri kabul edecek bir MERGEBARCODE alanı ekleyin.
// Bu alan, bir birleştirme veri kaynağının "MyEAN13Barcode" sütunundaki tüm değerleri EAN13 barkodlarına dönüştürecektir.
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

// MERGEBARCODE alanımızın BarcodeValue ile aynı ada sahip bir sütunu olan bir DataTable oluşturun.
// Adres mektup birleştirme, her satır için yeni bir sayfa oluşturacaktır. Her sayfa bir EKRAN BARKOD alanı içerecektir,
// birleştirilmiş satırdaki değerle birlikte bir EAN13 barkodu görüntüleyecektir.
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

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


