---
title: MailMergeRegionInfo.EndMustacheTag
linktitle: EndMustacheTag
articleTitle: EndMustacheTag
second_title: .NET için Aspose.Words
description: Belge bölgeleriniz için son bıyık etiketini verimli bir şekilde döndüren MailMergeRegionInfo EndMustacheTag özelliğini keşfedin. İş akışınızı optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/
---
## MailMergeRegionInfo.EndMustacheTag property

Bölge için bir "bıyık" etiketi sonu döndürür.

```csharp
public MustacheTag EndMustacheTag { get; }
```

## Örnekler

Bıyık etiketlerinin nasıl kullanılacağını gösterir.

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
