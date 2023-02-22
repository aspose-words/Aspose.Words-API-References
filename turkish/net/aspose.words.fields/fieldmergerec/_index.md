---
title: Class FieldMergeRec
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldMergeRec sınıf. MERGEREC alanını uygular.
type: docs
weight: 2010
url: /tr/net/aspose.words.fields/fieldmergerec/
---
## FieldMergeRec class

MERGEREC alanını uygular.

```csharp
public class FieldMergeRec : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldMergeRec](fieldmergerec/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | [`FieldFormat`](../fieldformat/) alanın biçimlendirmesine yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. null. olabilir |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
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

Şu anda MERGEREC ve MERGESEQ alanları aynı işlevselliği uyguluyor çünkü Aspose.Words adres mektup birleştirmede kayıtları nasıl atlayacağımızı kesin bilmiyoruz.

### Örnekler

Adres mektup birleştirmenin çıktı belgelerindeki adres mektup birleştirme kayıtlarını numaralandırmak ve saymak için MERGEREC ve MERGESEQ alanlarının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Bir MERGEREC alanı, her birleştirme çıktı belgesinde birleştirilen verilerin satır numarasını yazdıracaktır.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Bir MERGESEQ alanı, başarılı birleştirmelerin sayısını sayar ve geçerli değeri ilgili her sayfaya yazdırır.
// Adres mektup birleştirme hiçbir satırı atlamaz ve hiçbir SKIP/SKIPIF/NEXT/NEXTIF alanını çağırmazsa, tüm birleştirmeler başarılı olur.
// MERGESEQ ve MERGEREC alanları, adres mektup birleştirmenin başarılı olduğu aynı sonuçları görüntüleyecektir.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Adı "John Doe" ise birleştirmeyi atlayacak bir SKIPIF alanı ekleyin.
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Bir tanesi "Ad" sütunu için değer olarak "John Doe" olan 3 satırlı bir veri kaynağı oluşturun.
// Bir SKIPIF alanı bu değer tarafından bir kez tetikleneceğinden, adres mektup birleştirmemizin çıktısı 3 yerine 2 sayfa olacaktır.
// 1. sayfada, MERGESEQ ve MERGEREC alanlarının her ikisi de "1" gösterecektir.
// 2. sayfada, MERGEREC alanında "3" ve MERGESEQ alanında "2" görüntülenecektir.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


