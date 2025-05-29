---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: .NET için Aspose.Words
description: MergeDuplicateRegions özelliğiyle posta birleştirme işleminizi optimize edin. Verimli belge yönetimi için veri kaynağı bölgelerinin nasıl birleştirileceğini kontrol edin.
type: docs
weight: 60
url: /tr/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Veri kaynağına ait tüm belge birleştirme bölgelerinin, veri kaynağına ait bölgelerle veya yalnızca ilk bölgeyle bir birleştirme işlemi yürütülürken birleştirilip birleştirilmeyeceğini belirten bir değer alır veya ayarlar.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Yinelenen posta birleştirme bölgeleriyle nasıl çalışılacağını gösterir.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // "MergeDuplicateRegions" özelliğini "false" olarak ayarlarsak, posta birleştirme ilk bölgeyi etkileyecektir.
    // ikincisinin MERGEFIELD'ları ise birleştirme öncesi durumunda bırakılacak.
    // Her iki bölgeyi de bu şekilde birleştirmek için,
    // Aynı isimli tabloda posta birleştirmeyi iki kez yapmamız gerekir.
    // "MergeDuplicateRegions" özelliğini "true" olarak ayarlarsak, posta birleştirme her iki bölgeyi de etkileyecektir.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Aynı adı taşıyan ("TableStart/End" etiketlerinde) iki yinelenen posta birleştirme bölgesi içeren bir belge döndürür.
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// Bir satır ve iki sütundan oluşan bir veri tablosu oluşturur.
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Ayrıca bakınız

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
