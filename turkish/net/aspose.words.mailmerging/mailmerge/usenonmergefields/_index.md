---
title: MailMerge.UseNonMergeFields
second_title: Aspose.Words for .NET API Referansı
description: MailMerge mülk. Ne zamandoğru MERGEFIELD alanlarına ek olarak diğer bazı alan türlerinde ve ayrıca fieldName etiketlerinde adresmektup birleştirme işleminin gerçekleştirildiğini belirtir.
type: docs
weight: 150
url: /tr/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

Ne zaman`doğru` MERGEFIELD alanlarına ek olarak diğer bazı alan türlerinde ve ayrıca "{{fieldName}}" etiketlerinde adres-mektup birleştirme işleminin gerçekleştirildiğini belirtir.

```csharp
public bool UseNonMergeFields { get; set; }
```

### Notlar

Normalde, adres-mektup birleştirme yalnızca MERGEFIELD alanlarında gerçekleştirilir, ancak bazı müşterilerin kendi report 'leri diğer alanları kullanarak oluşturulmuş ve birçok belge bu şekilde oluşturulmuştur. Geçişi basitleştirmek için (ve this yaklaşımı birçok müşteri tarafından bağımsız olarak kullanıldığından) diğer alanlara adres-mektup birleştirme özelliği getirildi.

Ne zaman`UseNonMergeFields` ayarlandı`doğru`Aspose.Words aşağıdaki alanlarda adres-mektup birleştirme işlemini gerçekleştirecektir:

MERGEFIELD AlanAdı

MACROBUTTON NOMACRO AlanAdı

IF 0 = 0 "{FieldName}" ""

Ayrıca ne zaman`UseNonMergeFields` ayarlandı`doğru`Aspose.Words, tags "{{fieldName}}" metnine adres-mektup birleştirme işlemini gerçekleştirecektir. Bunlar alanlar değil, yalnızca metin etiketleridir.

### Örnekler

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

* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)


