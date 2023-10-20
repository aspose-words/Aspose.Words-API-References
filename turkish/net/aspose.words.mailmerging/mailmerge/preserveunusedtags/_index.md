---
title: MailMerge.PreserveUnusedTags
linktitle: PreserveUnusedTags
articleTitle: PreserveUnusedTags
second_title: Aspose.Words for .NET
description: MailMerge PreserveUnusedTags mülk. Kullanılmayan bıyık etiketlerinin korunması gerekip gerekmediğini belirten bir değer alır veya ayarlar C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

Kullanılmayan "bıyık" etiketlerinin korunması gerekip gerekmediğini belirten bir değer alır veya ayarlar.

```csharp
public bool PreserveUnusedTags { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Adres-mektup birleştirme sırasında kullanılmayan alternatif adres-mektup birleştirme etiketlerinin görünümünün nasıl korunacağını gösterir.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // Adres-mektup birleştirme, varsayılan olarak bir tablonun her satırındaki verileri, o tablodaki sütunları adlandıran MERGEFIELD'lere yerleştirir.
    // Belgemizde bu tür alanlar yok ancak küme parantezleri içine alınmış düz metin etiketleri var.
    // "PreserveUnusedTags" bayrağını "true" olarak ayarlarsak, bu etiketleri MERGEFIELD'ler olarak değerlendirebiliriz
    // adres-mektup birleştirmemizin bu etiketlere veri kaynağından veri eklemesine izin vermek için.
    // "PreserveUnusedTags" flagını "false" olarak ayarlarsak,
    // adres-mektup birleştirme bu etiketleri MERGEFIELD'lere dönüştürecek ve doldurulmamış bırakacaktır.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Belgemizde tabloda bulunmayan "Column2" adlı bir sütun için etiket bulunmaktadır.
    // "PreserveUnusedTags" flagını "false" olarak ayarlarsak, then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Bir belge oluşturun ve adres-mektup birleştirme sırasında MERGEFIELD işlevi görebilecek iki düz metin etiketi ekleyin.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Etiketlerimiz, yalnızca bunu true olarak ayarlarsak, adres-mektup birleştirme verileri için hedef olarak kaydedilecektir.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// Tek sütunlu basit bir veri tablosu oluşturun.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### Ayrıca bakınız

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
