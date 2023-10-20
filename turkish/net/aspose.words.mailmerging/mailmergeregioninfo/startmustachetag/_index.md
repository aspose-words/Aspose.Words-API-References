---
title: MailMergeRegionInfo.StartMustacheTag
linktitle: StartMustacheTag
articleTitle: StartMustacheTag
second_title: Aspose.Words for .NET
description: MailMergeRegionInfo StartMustacheTag mülk. Bölge için bir başlangıç bıyık etiketi döndürür C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

Bölge için bir başlangıç "bıyık" etiketi döndürür.

```csharp
public MustacheTag StartMustacheTag { get; }
```

## Örnekler

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
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
