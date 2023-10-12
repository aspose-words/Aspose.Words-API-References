---
title: MailMerge.MailMergeCallback
second_title: Aspose.Words for .NET API Referansı
description: MailMerge mülk. Adresmektup birleştirme sırasında belirli olayların işlenmesine izin verir.
type: docs
weight: 40
url: /tr/net/aspose.words.mailmerging/mailmerge/mailmergecallback/
---
## MailMerge.MailMergeCallback property

Adres-mektup birleştirme sırasında belirli olayların işlenmesine izin verir.

```csharp
public IMailMergeCallback MailMergeCallback { get; set; }
```

### Örnekler

Adres-mektup birleştirme sırasında olayların işlenmesi için özel mantığın nasıl tanımlanacağını gösterir.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir veri kaynağındaki iki sütuna başvuran iki adres-mektup birleştirme etiketi ekleyin.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Birleştirme etiketlerimizin referans verdiği sütunlardan yalnızca birini içeren bir veri kaynağı oluşturun.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Adres-mektup birleştirmemizi alternatif adres-mektup birleştirme etiketlerini kullanacak şekilde yapılandırın.
    doc.MailMerge.UseNonMergeFields = true;

    // Ardından, adres-mektup birleştirmenin "LastName" etiketimiz gibi etiketleri dönüştüreceğinden emin olun,
    // birleştirme belgelerindeki MERGEFIELD'lere.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Adres-mektup birleştirmenin, MERGEFIELD'lerle verilerle dolduramadığı adres-mektup birleştirme etiketlerini kaç kez değiştirdiğini sayar.
/// </summary>
private class MailMergeTagReplacementCounter : IMailMergeCallback
{
    public void TagsReplaced()
    {
        TagsReplacedCount++;
    }

    public int TagsReplacedCount { get; private set; }
}
```

### Ayrıca bakınız

* interface [IMailMergeCallback](../../imailmergecallback/)
* class [MailMerge](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmerge/)
* toplantı [Aspose.Words](../../../)


