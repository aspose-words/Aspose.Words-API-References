---
title: MailMergeRegionInfo.EndMustacheTag
linktitle: EndMustacheTag
articleTitle: EndMustacheTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die MailMergeRegionInfo-Eigenschaft EndMustacheTag, die effizient das End-Mustache-Tag für Ihre Dokumentbereiche zurückgibt. Optimieren Sie Ihren Workflow!
type: docs
weight: 20
url: /de/net/aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/
---
## MailMergeRegionInfo.EndMustacheTag property

Gibt ein End-„Mustache“-Tag für die Region zurück.

```csharp
public MustacheTag EndMustacheTag { get; }
```

## Beispiele

Zeigt, wie mit den Mustache-Tags gearbeitet wird.

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

### Siehe auch

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
