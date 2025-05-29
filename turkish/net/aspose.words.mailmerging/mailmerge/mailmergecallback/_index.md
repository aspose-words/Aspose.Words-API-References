---
title: MailMerge.MailMergeCallback
linktitle: MailMergeCallback
articleTitle: MailMergeCallback
second_title: .NET için Aspose.Words
description: MailMergeCallback özelliğiyle posta birleştirmenizi optimize edin. Sorunsuz belge otomasyonu ve gelişmiş verimlilik için olayları zahmetsizce yönetin.
type: docs
weight: 40
url: /tr/net/aspose.words.mailmerging/mailmerge/mailmergecallback/
---
## MailMerge.MailMergeCallback property

Posta birleştirme sırasında belirli olayların işlenmesine izin verir.

```csharp
public IMailMergeCallback MailMergeCallback { get; set; }
```

## Örnekler

Posta birleştirme sırasında olayların işlenmesi için özel mantığın nasıl tanımlanacağını gösterir.

```csharp
public void Callback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Bir veri kaynağındaki iki sütuna başvuran iki posta birleştirme etiketi ekleyin.
    builder.Write("{{FirstName}}");
    builder.Write("{{LastName}}");

    // Birleştirme etiketlerimizin başvurduğu sütunlardan yalnızca birini içeren bir veri kaynağı oluşturun.
    DataTable table = new DataTable("Test");
    table.Columns.Add("FirstName");
    table.Rows.Add("John");
    table.Rows.Add("Jane");

    // Posta birleştirmemizi alternatif posta birleştirme etiketlerini kullanacak şekilde yapılandırın.
    doc.MailMerge.UseNonMergeFields = true;

    // Ardından, posta birleştirmenin "Soyadı" etiketi gibi etiketleri dönüştüreceğinden emin olun.
    // birleştirme belgelerindeki MERGEFIELD'lara.
    doc.MailMerge.PreserveUnusedTags = false;

    MailMergeTagReplacementCounter counter = new MailMergeTagReplacementCounter();
    doc.MailMerge.MailMergeCallback = counter;
    doc.MailMerge.Execute(table);

    Assert.AreEqual(1, counter.TagsReplacedCount);
}

/// <summary>
/// Bir posta birleştirme işleminin, MERGEFIELD'lerle veriyle dolduramadığı posta birleştirme etiketlerini kaç kez değiştirdiğini sayar.
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
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
