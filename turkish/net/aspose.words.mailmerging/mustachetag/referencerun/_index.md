---
title: MustacheTag.ReferenceRun
second_title: Aspose.Words for .NET API Referansı
description: MustacheTag mülk. Etiketin başlangıcını içeren çalıştırmayı alır.
type: docs
weight: 20
url: /tr/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Etiketin başlangıcını içeren çalıştırmayı alır.

```csharp
public Run ReferenceRun { get; }
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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* ad alanı [Aspose.Words.MailMerging](../../mustachetag/)
* toplantı [Aspose.Words](../../../)


