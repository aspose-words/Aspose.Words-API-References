---
title: IMailMergeCallback.TagsReplaced
linktitle: TagsReplaced
articleTitle: TagsReplaced
second_title: .NET için Aspose.Words
description: IMailMergeCallback TagsReplaced yönteminin bıyık metnini MERGEFIELD alanlarıyla sorunsuz bir şekilde değiştirerek belge otomasyonunuzu nasıl geliştirdiğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.mailmerging/imailmergecallback/tagsreplaced/
---
## IMailMergeCallback.TagsReplaced method

"Mustache" metin etiketleri MERGEFIELD alanlarıyla değiştirildiğinde çağrılır.

```csharp
public void TagsReplaced()
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

* property [UseNonMergeFields](../../mailmerge/usenonmergefields/)
* interface [IMailMergeCallback](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
