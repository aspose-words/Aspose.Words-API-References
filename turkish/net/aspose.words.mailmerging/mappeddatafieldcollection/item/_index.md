---
title: MappedDataFieldCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Sorunsuz posta birleştirme entegrasyonu için veri kaynağınızdaki alan adlarını kolayca yönetmek üzere MappedDataFieldCollection Öğesi özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/mappeddatafieldcollection/item/
---
## MappedDataFieldCollection indexer

Belirtilen posta birleştirme alanıyla ilişkili veri kaynağındaki alanın adını alır veya ayarlar.

```csharp
public string this[string documentFieldName] { get; set; }
```

## Örnekler

Bir posta birleştirme sırasında verilerin aralarında aktarılması için veri sütunlarının ve MERGEFIELD'ların farklı adlarla nasıl eşleneceğini gösterir.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // Tabloda "Column2" adında bir sütun var, ancak bu isimde bir MERGEFIELD yok.
    // Ayrıca, "Column3" adında bir MERGEFIELD'ımız var, ancak veri kaynağında bu isimde bir sütun bulunmuyor.
    // "Column2"deki veriler "Column3" MERGEFIELD'ı için uygunsa,
    // bu sütun adını "MappedDataFields" anahtar/değer çiftindeki MERGEFIELD'a eşleyebiliriz.
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Bir veri kaynağı sütun adını bir MERGEFIELD adına şu şekilde bağlayabiliriz.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // "Column2" adlı veri kaynağı sütununu "Column3" adlı MERGEFIELD'lara bağla.
    mappedDataFields.Add("Column3", "Column2");

    // MERGEFIELD adı, ilgili veri kaynağı sütun adı olan "değer"in "anahtarı"dır.
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Şimdi bu posta birleştirmeyi çalıştırırsak, "Sütun3" MERGEFIELD'ları tablonun "Sütun2"sinden veri alacaktır.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Bu koleksiyondaki elemanlar üzerinde yineleme yapabiliriz.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // Ayrıca koleksiyondan öğeleri kaldırabiliriz.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// 2 MERGEFIELD içeren bir belge oluşturun, bunlardan biri
/// Aşağıdaki yöntemden veri tablosundaki karşılık gelen sütun.
/// </summary>
private static Document CreateSourceDocMappedDataFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column3");

    return doc;
}

/// <summary>
/// 2 sütundan oluşan bir veri tablosu oluşturun, bunlardan birinde sütun yok
/// Yukarıdaki yönteme ait kaynak belgedeki karşılık gelen MERGEFIELD.
/// </summary>
private static DataTable CreateSourceTableMappedDataFields()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value1", "Value2" });

    return dataTable;
}
```

### Ayrıca bakınız

* class [MappedDataFieldCollection](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
