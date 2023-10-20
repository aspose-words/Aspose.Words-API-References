---
title: MustacheTag.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: MustacheTag Text mülk. Etiketin metnini alır C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Etiketin metnini alır.

```csharp
public string Text { get; }
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

* class [MustacheTag](../)
* ad alanı [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../../)
