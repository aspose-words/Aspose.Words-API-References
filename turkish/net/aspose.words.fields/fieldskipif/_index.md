---
title: FieldSkipIf Class
linktitle: FieldSkipIf
articleTitle: FieldSkipIf
second_title: .NET için Aspose.Words
description: Projelerinizde belge otomasyonunu ve esnekliğini artırarak SKIPIF alanlarını etkili bir şekilde uygulamak için Aspose.Words.Fields.FieldSkipIf sınıfını keşfedin.
type: docs
weight: 2830
url: /tr/net/aspose.words.fields/fieldskipif/
---
## FieldSkipIf class

SKIPIF alanını uygular.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

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
| [Format](../../aspose.words.fields/field/format/) { get; } | Bir tane alır[`FieldFormat`](../fieldformat/)alanın biçimlendirmesine yazılmış erişim sağlayan nesne. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Belgede yapılan diğer değişiklikler nedeniyle alanın geçerli sonucunun artık doğru (eski) olup olmadığını alır veya ayarlar. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Alanın kilitli olup olmadığını alır veya ayarlar (sonucunu yeniden hesaplamamalıdır). |
| [LeftExpression](../../aspose.words.fields/fieldskipif/leftexpression/) { get; set; } | Karşılaştırma ifadesinin sol kısmını alır veya ayarlar. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Alanın LCID'sini alır veya ayarlar. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Alan ayırıcısı ile alan sonu arasındaki metni alır veya ayarlar. |
| [RightExpression](../../aspose.words.fields/fieldskipif/rightexpression/) { get; set; } | Karşılaştırma ifadesinin doğru kısmını alır veya ayarlar. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Alan ayırıcısını temsil eden düğümü alır.`hükümsüz` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Alanın başlangıcını temsil eden düğümü alır. |
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

İfadelerle belirtilen değerleri karşılaştırır[`LeftExpression`](./leftexpression/) Ve[`RightExpression`](./rightexpression/) ile belirtilen operatör kullanılarak karşılaştırma[`ComparisonOperator`](./comparisonoperator/) . Karşılaştırma doğruysa, SKIPIF geçerli birleştirme belgesini iptal eder, veri kaynağındaki bir sonraki veri kaydına geçer ve yeni bir birleştirme belgesi başlatır. Karşılaştırma yanlışsa, geçerli birleştirme belgesi devam eder.

## Örnekler

SKIPIF alanını kullanarak bir posta birleştirmede sayfaların nasıl atlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir SKIPIF alanı ekleyin. Bir posta birleştirme işleminin geçerli satırı koşulu karşılıyorsa
// bu alanın ifadeleri neyi belirtiyorsa, posta birleştirme işlemi geçerli satırı iptal eder,
// geçerli birleştirme belgesini siler ve hemen bir sonraki birleştirme belgesine başlamak için bir sonraki satıra geçer.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// SKIPIF alanının ayırıcısına oluşturucuyu taşıyalım, böylece SKIPIF alanının içine bir MERGEFIELD yerleştirebiliriz.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD, veri tablomuzdaki "Departman" sütununa atıfta bulunur. Bu tablodan bir satır
// "Departman" sütununda "HR" değeri varsa, bu satır koşulu sağlayacaktır.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Belgemize içerik ekleyin, veri kaynağını oluşturun ve posta birleştirmeyi gerçekleştirin.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // Bu tablonun üç satırı var ve bunlardan biri SKIPIF alanımızın koşulunu sağlıyor.
// Posta birleştirme işlemi iki sayfa üretecektir.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Bir posta birleştirme işleminin çıktı belgelerinde, MERGEREC ve MERGESEQ alanlarının posta birleştirme kayıtlarını numaralandırmak ve saymak için nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// MERGEREC alanı, her birleştirme çıktı belgesinde birleştirilecek verilerin satır numarasını yazdıracaktır.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// MERGESEQ alanı başarılı birleştirmelerin sayısını sayar ve her ilgili sayfada geçerli değeri yazdırır.
// Bir posta birleştirme işlemi hiçbir satırı atlamıyorsa ve hiçbir SKIP/SKIPIF/NEXT/NEXTIF alanını çağırmıyorsa, tüm birleştirmeler başarılıdır.
// MERGESEQ ve MERGEREC alanları, posta birleştirme işlemi başarılı olursa aynı sonuçları görüntüler.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// İsim "John Doe" ise birleştirmeyi atlayacak bir SKIPIF alanı ekleyin.
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// 3 satırdan oluşan bir veri kaynağı oluşturun, bunlardan birinde "Ad" sütunu için değer olarak "John Doe" bulunsun.
// SKIPIF alanı bu değer tarafından bir kez tetikleneceğinden, posta birleştirme çıktımız 3 yerine 2 sayfa olacaktır.
// 1. sayfada MERGESEQ ve MERGEREC alanlarının her ikisinde de "1" görüntülenecektir.
// 2. sayfada MERGEREC alanı "3" değerini, MERGESEQ alanı ise "2" değerini gösterecektir.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add("Jane Doe");
table.Rows.Add("John Doe");
table.Rows.Add("Joe Bloggs");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Ayrıca bakınız

* class [Field](../field/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
