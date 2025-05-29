---
title: FieldSkipIf.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: .NET için Aspose.Words
description: FieldSkipIf ComparisonOperator özelliğini keşfedin, gelişmiş veri işleme için karşılaştırma operatörlerinizi kolayca yönetin ve özelleştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldskipif/comparisonoperator/
---
## FieldSkipIf.ComparisonOperator property

Karşılaştırma operatörünü alır veya ayarlar.

```csharp
public string ComparisonOperator { get; set; }
```

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

* class [FieldSkipIf](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
