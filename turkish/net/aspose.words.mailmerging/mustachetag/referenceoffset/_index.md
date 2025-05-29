---
title: MustacheTag.ReferenceOffset
linktitle: ReferenceOffset
articleTitle: ReferenceOffset
second_title: .NET için Aspose.Words
description: ReferenceRun'ınızdaki etiketlerin sıfır tabanlı başlangıç konumunu ortaya çıkaran MustacheTag ReferenceOffset özelliğini keşfedin ve böylece hassas veri yönetimi sağlayın.
type: docs
weight: 10
url: /tr/net/aspose.words.mailmerging/mustachetag/referenceoffset/
---
## MustacheTag.ReferenceOffset property

Etiketin sıfır tabanlı başlangıç konumunu, etiketin başlangıcından itibaren alır.[`ReferenceRun`](../referencerun/) .

```csharp
public int ReferenceOffset { get; }
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

* class [MustacheTag](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
