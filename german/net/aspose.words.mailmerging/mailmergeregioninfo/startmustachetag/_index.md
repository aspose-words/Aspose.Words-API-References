---
title: MailMergeRegionInfo.StartMustacheTag
linktitle: StartMustacheTag
articleTitle: StartMustacheTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die StartMustacheTag-Eigenschaft von MailMergeRegionInfo, die ein wichtiges Start-Tag für nahtlose Dokumentbereiche in Ihren Projekten bereitstellt.
type: docs
weight: 100
url: /de/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

Gibt ein Start-Tag „mustache“ für die Region zurück.

```csharp
public MustacheTag StartMustacheTag { get; }
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
