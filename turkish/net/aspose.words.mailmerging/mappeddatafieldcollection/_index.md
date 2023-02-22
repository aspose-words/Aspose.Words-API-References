---
title: Class MappedDataFieldCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.MailMerging.MappedDataFieldCollection sınıf. Veri kaynağınızdaki alanların adlarıyla belgedeki adres mektup birleştirme alanlarının adları arasında otomatik olarak eşleme yapmanızı sağlar.
type: docs
weight: 3650
url: /tr/net/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class

Veri kaynağınızdaki alanların adlarıyla belgedeki adres mektup birleştirme alanlarının adları arasında otomatik olarak eşleme yapmanızı sağlar.

```csharp
public class MappedDataFieldCollection : IEnumerable<KeyValuePair<string, string>>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.mailmerging/mappeddatafieldcollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.mailmerging/mappeddatafieldcollection/item/) { get; set; } | Belirtilen adres mektup birleştirme alanıyla ilişkili veri kaynağındaki alanın adını alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.mailmerging/mappeddatafieldcollection/add/)(string, string) | Yeni bir alan eşlemesi ekler. |
| [Clear](../../aspose.words.mailmerging/mappeddatafieldcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [ContainsKey](../../aspose.words.mailmerging/mappeddatafieldcollection/containskey/)(string) | Belgede belirtilen alandan bir eşlemenin koleksiyonda bulunup bulunmadığını belirler. |
| [ContainsValue](../../aspose.words.mailmerging/mappeddatafieldcollection/containsvalue/)(string) | Koleksiyonda veri kaynağında belirtilen alandan bir eşleme olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words.mailmerging/mappeddatafieldcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir sözlük numaralandırıcı nesnesi döndürür. |
| [Remove](../../aspose.words.mailmerging/mappeddatafieldcollection/remove/)(string) | Bir alan eşlemesini kaldırır. |

### Notlar

Bu, dize anahtarlarının dize değerlerine bir koleksiyonu olarak uygulanır. Anahtarlar, belgedeki adres mektup birleştirme alanlarının adlarıdır ve değerler , veri kaynağınızdaki alanların adlarıdır.

### Örnekler

Adres mektup birleştirme sırasında verilerin aralarında aktarılması için farklı adlara sahip veri sütunlarının ve MERGEFIELD'lerin nasıl eşleneceğini gösterir.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // Tabloda "Sütun2" adında bir sütun var, ancak bu ada sahip MERGEFIELD yok.
    // Ayrıca, "Column3" adında bir MERGEFIELD'imiz var, ancak veri kaynağında bu ada sahip bir sütun yok.
    // "Sütun2"den gelen veriler "Sütun3" MERGEFIELD için uygunsa,
    // bu sütun adını "MappedDataFields" anahtar/değer çiftindeki MERGEFIELD ile eşleştirebiliriz.
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Bir veri kaynağı sütun adını şu şekilde bir MERGEFIELD adına bağlayabiliriz.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // "Column2" adlı veri kaynağı sütununu "Column3" adlı MERGEFIELD'lere bağlayın.
    mappedDataFields.Add("Column3", "Column2");

    // MERGEFIELD adı, ilgili veri kaynağı sütun adı "değer" için "anahtar"dır.
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Şimdi bu adres mektup birleştirmeyi çalıştırırsak, "Sütun3" MERGEFIELD'leri tablonun "Sütun2" sinden veri alacaktır.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Bu koleksiyondaki öğeleri yineleyebiliriz.
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
/// 2 MERGEFIELD içeren bir belge oluşturun, bunlardan biri
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
/// 2 sütunlu bir veri tablosu oluşturun.
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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)


