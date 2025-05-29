---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: .NET için Aspose.Words
description: MailMerge'in UnconditionalMergeFieldsAndRegions özelliğinin koşullu sınırlamalar olmadan alanları ve bölgeleri birleştirerek belge otomasyonunu nasıl geliştirdiğini keşfedin.
type: docs
weight: 140
url: /tr/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Üst IF alanının koşulundan bağımsız olarak birleştirme alanlarının ve birleştirme bölgelerinin birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Üst IF alanının koşulundan bağımsız olarak alanların veya bölgelerin nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir IF alanının içine yerleştirilmiş bir MERGEFIELD ekle.
// IF alan ifadesi yanlış olduğundan MERGEFIELD'ın sonucu görüntülenmeyecektir.
// MERGEFIELD ayrıca posta birleştirme sırasında herhangi bir veri almayacaktır.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// "UnconditionalMergeFieldsAndRegions" bayrağını "true" olarak ayarlarsak,
// birleştirme işlemimiz, MERGEFIELD alanımızın yanı sıra diğer tüm görüntülenmeyen alanlara da veri ekleyecektir.
// "UnconditionalMergeFieldsAndRegions" bayrağını "false" olarak ayarlarsak,
// birleştirme işlemimiz, false ifadeleri içeren IF alanlarıyla gizlenen MERGEFIELD'lara veri eklemeyecektir.
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
