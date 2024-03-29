---
title: FieldSkipIf Class
linktitle: FieldSkipIf
articleTitle: FieldSkipIf
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldSkipIf sınıf. SKIPIF alanını uygular C#'da.
type: docs
weight: 2420
url: /tr/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

SKIPIF alanını uygular.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class FieldSkipIf : Field
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FieldSkipIf](fieldskipif/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldskipif/comparisonoperator/) { get; set; } | Karşılaştırma operatörünü alır veya ayarlar. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Görüntülenen alan sonucunu temsil eden metni alır. |
| [End](../../aspose.words.fields/field/end/) { get; } | Alan sonunu temsil eden düğümü alır. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir alır[`FieldFormat`](../fieldformat/) Alanın formatlamasına yazılı erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucu yeniden hesaplanmamalıdır). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | Karşılaştırma ifadesinin sol kısmını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcı ile alan sonu arasındaki metni alır veya ayarlar. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | Karşılaştırma ifadesinin doğru kısmını alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcıyı temsil eden düğümü alır. Olabilir`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Microsoft Word alan türünü alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. Alt alanların hem alan kodu hem de alan sonucu dahil edilir. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Alan başlangıcı ile alan ayırıcı (veya ayırıcı yoksa alan sonu) arasındaki metni döndürür. |
| [Remove](../../aspose.words.fields/field/remove/)() | Alanı belgeden kaldırır. Alanın hemen ardından bir düğüm döndürür. Alanın sonu, üst düğümünün son child 'si ise, üst paragrafını döndürür. Alan zaten kaldırılmışsa şunu döndürür:`hükümsüz` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Alanın bağlantısını kaldırır. |
| [Update](../../aspose.words.fields/field/update/)() | Alan güncellemesini gerçekleştirir. Alan zaten güncelleniyorsa atar. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Bir alan güncellemesi gerçekleştirir. Alan zaten güncelleniyorsa atar. |

## Notlar

İfadelerin belirlediği değerleri karşılaştırır[`LeftExpression`](./leftexpression/) Ve[`RightExpression`](./rightexpression/) ile belirtilen operatör kullanılarak karşılaştırıldığında[`ComparisonOperator`](./comparisonoperator/) . Karşılaştırma doğruysa SKIPIF geçerli birleştirme belgesini iptal eder, veri kaynağındaki bir sonraki veri kaydına geçer ve yeni bir birleştirme belgesi başlatır. Karşılaştırma yanlışsa geçerli birleştirme belgesine devam edilir.

## Örnekler

SKIPIF alanını kullanarak adres-mektup birleştirmede sayfaların nasıl atlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir SKIPIF alanı ekleyin. Adres-mektup birleştirme işleminin geçerli satırı koşulu karşılıyorsa
// bu alanın ifadeleri hangi durumdaysa, adres-mektup birleştirme işlemi geçerli satırı iptal eder,
// geçerli birleştirme belgesini atar ve ardından bir sonraki birleştirme belgesine başlamak için hemen bir sonraki satıra geçer.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Oluşturucuyu SKIPIF alanının ayırıcısına taşıyın, böylece SKIPIF alanının içine bir MERGEFIELD yerleştirebiliriz.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD veri tablomuzdaki "Departman" sütununu ifade eder. Eğer o tablodan bir satır
// "Departman" sütununda "HR" değeri varsa bu satır koşulu yerine getirecektir.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Belgemize içerik ekleyin, veri kaynağını oluşturun ve adres-mektup birleştirmeyi yürütün.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // Bu tablonun üç satırı var ve bunlardan biri SKIPIF alanımızın koşulunu yerine getiriyor.
// Adres-mektup birleştirme iki sayfa oluşturacaktır.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Adres-mektup birleştirmenin çıktı belgelerindeki adres-mektup birleştirme kayıtlarını numaralandırmak ve saymak için MERGEREC ve MERGESEQ alanlarının nasıl kullanılacağını gösterir.

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

// MERGESEQ alanı başarılı birleştirmelerin sayısını sayar ve geçerli değeri ilgili her sayfaya yazdırır.
// Adres-mektup birleştirme hiçbir satırı atlamıyorsa ve hiçbir SKIP/SKIPIF/NEXT/NEXTIF alanını çağırmıyorsa, tüm birleştirmeler başarılı olur.
// MERGESEQ ve MERGEREC alanları, adres-mektup birleştirme başarılı olduğunda aynı sonuçları gösterecektir.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Adın "John Doe" olması durumunda birleştirmeyi atlayacak bir SKIPIF alanı ekleyin.
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// 3 satırlı bir veri kaynağı oluşturun; bunlardan birinde "Ad" sütununun değeri "John Doe"dur.
// Bir SKIPIF alanı bu değer tarafından bir kez tetikleneceğinden, adres-mektup birleştirmemizin çıktısı 3 yerine 2 sayfadan oluşacaktır.
// 1. sayfada, MERGESEQ ve MERGEREC alanlarının her ikisi de "1" gösterecektir.
// 2. sayfada MERGEREC alanında "3", MERGESEQ alanında ise "2" görüntülenecektir.
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
