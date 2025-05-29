---
title: MappedDataFieldCollection Class
linktitle: MappedDataFieldCollection
articleTitle: MappedDataFieldCollection
second_title: .NET için Aspose.Words
description: Veri kaynağı alanlarının posta birleştirme alanlarına kusursuz şekilde eşlenmesi ve belge otomasyonunun artırılması için Aspose.Words.MailMerging.MappedDataFieldCollection'ı keşfedin.
type: docs
weight: 4560
url: /tr/net/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class

Veri kaynağınızdaki alan adları ile belgedeki posta birleştirme alanlarının adları arasında otomatik olarak eşleme yapmanızı sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Posta Birleştirme ve Raporlama](https://docs.aspose.com/words/net/mail-merge-and-reporting/) belgeleme makalesi.

```csharp
public class MappedDataFieldCollection : IEnumerable<KeyValuePair<string, string>>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.mailmerging/mappeddatafieldcollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.mailmerging/mappeddatafieldcollection/item/) { get; set; } | Belirtilen posta birleştirme alanıyla ilişkili veri kaynağındaki alanın adını alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.mailmerging/mappeddatafieldcollection/add/)(*string, string*) | Yeni bir alan eşlemesi ekler. |
| [Clear](../../aspose.words.mailmerging/mappeddatafieldcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [ContainsKey](../../aspose.words.mailmerging/mappeddatafieldcollection/containskey/)(*string*) | Belgedeki belirtilen alandan bir eşlemenin koleksiyonda bulunup bulunmadığını belirler. |
| [ContainsValue](../../aspose.words.mailmerging/mappeddatafieldcollection/containsvalue/)(*string*) | Veri kaynağındaki belirtilen alandan bir eşlemenin koleksiyonda bulunup bulunmadığını belirler. |
| [GetEnumerator](../../aspose.words.mailmerging/mappeddatafieldcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir sözlük numaralandırıcı nesnesi döndürür. |
| [Remove](../../aspose.words.mailmerging/mappeddatafieldcollection/remove/)(*string*) | Bir alan eşlemesini kaldırır. |

## Notlar

Bu, dize anahtarlarının dize değerlerine dönüştürülmesiyle uygulanır. Anahtarlar, belgedeki birleştirme alanlarının adlarıdır ve values ise veri kaynağınızdaki alanların adlarıdır.

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

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
