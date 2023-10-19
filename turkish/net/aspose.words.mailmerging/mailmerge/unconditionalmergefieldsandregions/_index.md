---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words for .NET
description: MailMerge UnconditionalMergeFieldsAndRegions mülk. Ana IF alanının durumuna bakılmaksızın birleştirme alanları ve birleştirme bölgelerinin birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar C#'da.
type: docs
weight: 140
url: /tr/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Ana IF alanının durumuna bakılmaksızın birleştirme alanları ve birleştirme bölgelerinin birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Üst IF alanının durumuna bakılmaksızın alanların veya bölgelerin nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// IF alanının içine yerleştirilmiş bir MERGEFIELD ekleyin.
// IF alanı ifadesi yanlış olduğundan MERGEFIELD sonucunu göstermez.
// MERGEFIELD adres-mektup birleştirme sırasında da herhangi bir veri almayacaktır.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// "UnconditionalMergeFieldsAndRegions" flagını "true" olarak ayarlarsak,
// adres-mektup birleştirmemiz, MERGEFIELD ve diğerleri gibi görüntülenmeyen alanlara veri ekleyecektir.
// "UnconditionalMergeFieldsAndRegions" flagını "false" olarak ayarlarsak,
// adres-mektup birleştirmemiz, yanlış ifadelere sahip IF alanları tarafından gizlenen MERGEFIELD'lere veri eklemeyecektir.
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
