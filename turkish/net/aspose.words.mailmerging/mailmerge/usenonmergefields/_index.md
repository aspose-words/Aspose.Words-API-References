---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: .NET için Aspose.Words
description: MailMerge'in gücünü açığa çıkarın! Belgelerinizi çeşitli alan türlerine sorunsuz bir şekilde birleştirerek geliştirmek için UseNonMergeFields özelliğini kullanın.
type: docs
weight: 150
url: /tr/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

Ne zaman`doğru` , MERGEFIELD alanlarına ek olarak, bazı diğer alan türlerinde ve ayrıca "{{fieldName}}" etiketlerinde posta birleştirmenin gerçekleştirildiğini belirtir.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Notlar

Normalde, posta birleştirme yalnızca MERGEFIELD alanlarına yapılır, ancak birkaç müşterinin reporting 'si diğer alanları kullanarak oluşturulmuştu ve birçok belge bu şekilde oluşturulmuştu. Göçü basitleştirmek için (ve this yaklaşımı birkaç müşteri tarafından bağımsız olarak kullanıldığı için) diğer alanlara posta birleştirme yeteneği tanıtıldı.

Ne zaman`UseNonMergeFields` ayarlandı`doğru`, Aspose.Words aşağıdaki alanlarda posta birleştirme işlemini gerçekleştirecektir:

MERGEFIELD AlanAdı

MAKRO DÜĞME NOMACRO AlanAdı

EĞER 0 = 0 "{AlanAdı}" ""

Ayrıca, ne zaman`UseNonMergeFields` ayarlandı`doğru`, Aspose.Words, tags "{{fieldName}}" metnine posta birleştirme işlemi yapacaktır. Bunlar alan değil, sadece metin etiketleridir.

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

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
