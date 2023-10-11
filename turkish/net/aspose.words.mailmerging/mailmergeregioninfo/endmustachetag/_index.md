---
title: MailMergeRegionInfo.EndMustacheTag
second_title: Aspose.Words for .NET API Referansı
description: MailMergeRegionInfo mülk. Bölge için bir bitiş bıyık etiketi döndürür.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/
---
## MailMergeRegionInfo.EndMustacheTag property

Bölge için bir bitiş "bıyık" etiketi döndürür.

```csharp
public MustacheTag EndMustacheTag { get; }
```

### Örnekler

Bıyık etiketleriyle nasıl çalışılacağını gösterir.

```csharp
Document document = new Document(MyDir + "Mail merge mustache tags.docx");
document.MailMerge.UseNonMergeFields = true;

MailMergeRegionInfo hierarchy = document.MailMerge.GetRegionsHierarchy();

foreach (MustacheTag mustacheTag in hierarchy.MustacheTags)
{
    Console.WriteLine(mustacheTag.Text);
    Console.WriteLine(mustacheTag.ReferenceOffset);
    Console.WriteLine(mustacheTag.ReferenceRun);
}

foreach (MailMergeRegionInfo region in hierarchy.Regions)
{
    Console.WriteLine(region.StartMustacheTag.Text);
    Console.WriteLine(region.EndMustacheTag.Text);
}
```

### Ayrıca bakınız

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* ad alanı [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* toplantı [Aspose.Words](../../../)


