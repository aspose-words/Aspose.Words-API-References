---
title: MailMerge.PreserveUnusedTags
linktitle: PreserveUnusedTags
articleTitle: PreserveUnusedTags
second_title: .NET için Aspose.Words
description: Kullanılmayan bıyık etiketlerini etkili bir şekilde yönetmek ve belge otomasyon sürecinizi geliştirmek için MailMerge PreserveUnusedTags özelliğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

Kullanılmayan "mustache" etiketlerinin korunup korunmayacağını belirten bir değer alır veya ayarlar.

```csharp
public bool PreserveUnusedTags { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Bir posta birleştirme sırasında kullanılmayan alternatif posta birleştirme etiketlerinin görünümünün nasıl korunacağını gösterir.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // Varsayılan olarak, bir posta birleştirme işlemi bir tablonun her satırındaki verileri, o tablodaki sütunları adlandıran MERGEFIELD'lara yerleştirir.
    // Belgemizde böyle alanlar yok, ancak süslü parantezlerle çevrili düz metin etiketleri var.
    // "PreserveUnusedTags" bayrağını "true" olarak ayarlarsak, bu etiketleri MERGEFIELD'ler olarak ele alabiliriz
    // birleştirme işlemimizin veri kaynağındaki verileri bu etiketlere eklemesine izin vermek için.
    // "PreserveUnusedTags" bayrağını "false" olarak ayarlarsak,
    // posta birleştirme bu etiketleri MERGEFIELD'lara dönüştürecek ve doldurulmamış bırakacaktır.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Belgemizde tabloda bulunmayan "Column2" isimli bir sütuna ait etiket var.
    // "PreserveUnusedTags" bayrağını "false" olarak ayarlarsak, then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Bir belge oluşturun ve posta birleştirme sırasında MERGEFIELD işlevi görebilecek iki düz metin etiketi ekleyin.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Etiketlerimiz yalnızca bunu true olarak ayarlarsak posta birleştirme verileri için hedef olarak kaydedilecektir.
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
