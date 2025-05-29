---
title: MailMergeRegionInfo.StartMustacheTag
linktitle: StartMustacheTag
articleTitle: StartMustacheTag
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MailMergeRegionInfo StartMustacheTag, которое обеспечивает важный начальный тег для бесшовных областей документа в ваших проектах.
type: docs
weight: 100
url: /ru/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

Возвращает начальный тег «усы» для региона.

```csharp
public MustacheTag StartMustacheTag { get; }
```

## Примеры

Показывает, как работать с бирками-усами.

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

### Смотрите также

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
