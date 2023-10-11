---
title: MappedDataFieldCollection.Clear
second_title: Aspose.Words for .NET API Referansı
description: MappedDataFieldCollection yöntem. Koleksiyondaki tüm öğeleri kaldırır.
type: docs
weight: 40
url: /tr/net/aspose.words.mailmerging/mappeddatafieldcollection/clear/
---
## MappedDataFieldCollection.Clear method

Koleksiyondaki tüm öğeleri kaldırır.

```csharp
public void Clear()
```

### Örnekler

Adres-mektup birleştirme sırasında verilerin aralarında aktarılması için veri sütunlarının ve MERGEFIELD'lerin farklı adlarla nasıl eşleneceğini gösterir.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // Tabloda "Column2" adında bir sütun var ancak bu adda MERGEFIELD yok.
    // Ayrıca "Column3" adında bir MERGEFIELD'ımız var ancak veri kaynağında bu isimde bir sütun yok.
    // "Sütun2"deki veriler "Sütun3" MERGEFIELD için uygunsa,
    // bu sütun adını "MappedDataFields" anahtar/değer çiftindeki MERGEFIELD ile eşleyebiliriz.
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Bir veri kaynağı sütun adını bunun gibi bir MERGEFIELD ismine bağlayabiliriz.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // "Column2" adlı veri kaynağı sütununu "Column3" adlı MERGEFIELD'lere bağlayın.
    mappedDataFields.Add("Column3", "Column2");

    // MERGEFIELD adı, ilgili veri kaynağı sütun adı "değer"in "anahtarıdır".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Şimdi bu adres-mektup birleştirmeyi çalıştırırsak, "Sütun3" MERGEFIELD'ler tablonun "Sütun2"sinden veri alacaktır.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Bu koleksiyondaki öğeler üzerinde yineleme yapabiliriz.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // Koleksiyondan öğeleri de kaldırabiliriz.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// 2 MERGEFIELD içeren bir belge oluşturun, bunlardan birinde MERGEFIELD yok
/// aşağıdaki yöntemden veri tablosundaki ilgili sütun.
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
/// 2 sütunlu bir veri tablosu oluşturun, bunlardan birinde sütun yok
/// yukarıdaki yöntemden kaynak belgede karşılık gelen MERGEFIELD.
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
* ad alanı [Aspose.Words.MailMerging](../../mappeddatafieldcollection/)
* toplantı [Aspose.Words](../../../)


