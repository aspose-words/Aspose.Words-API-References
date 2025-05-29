---
title: MustacheTag.ReferenceRun
linktitle: ReferenceRun
articleTitle: ReferenceRun
second_title: .NET için Aspose.Words
description: MustacheTag ReferenceRun'ı keşfedin. Sorunsuz veri yönetimi ve gelişmiş performans için etiketinizin başlangıcını işaretleyen çalışmaya erişin.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Etiketin başlangıcını içeren çalışmayı alır.

```csharp
public Run ReferenceRun { get; }
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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
