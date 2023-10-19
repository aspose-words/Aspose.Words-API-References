---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words for .NET
description: MailMerge MergeDuplicateRegions mülk. Veri kaynağına karşı bölgelerle adresmektup birleştirme yürütülürken veri kaynağı adına sahip tüm belge adresmektup birleştirme bölgelerinin mi yoksa yalnızca ilkinin mi birleştirilmesi gerektiğini belirten bir değer alır veya ayarlar C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Veri kaynağına karşı bölgelerle adres-mektup birleştirme yürütülürken, veri kaynağı adına sahip tüm belge adres-mektup birleştirme bölgelerinin mi yoksa yalnızca ilkinin mi birleştirilmesi gerektiğini belirten bir değer alır veya ayarlar.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Yinelenen adres-mektup birleştirme bölgeleriyle nasıl çalışılacağını gösterir.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // "MergeDuplicateRegions" özelliğini "false" olarak ayarlarsak adres-mektup birleştirme ilk bölgeyi etkileyecektir,
    // ikincisinin MERGEFIELD'leri birleştirme öncesi durumda bırakılacak.
    // Her iki bölgeyi bu şekilde birleştirmek için,
    // aynı isimdeki bir tabloda adres-mektup birleştirme işlemini iki kez yürütmemiz gerekir.
    // "MergeDuplicateRegions" özelliğini "true" olarak ayarlarsak, adres-mektup birleştirme her iki bölgeyi de etkileyecektir.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// İki yinelenen adres-mektup birleştirme bölgesi içeren bir belge döndürür ("TableStart/End" etiketlerinde aynı adı paylaşır).
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
