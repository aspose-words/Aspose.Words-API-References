---
title: MailMergeRegionInfo.StartMustacheTag
second_title: Справочник по API Aspose.Words для .NET
description: MailMergeRegionInfo свойство. Возвращает начальный тег усы для региона.
type: docs
weight: 100
url: /ru/net/aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/
---
## MailMergeRegionInfo.StartMustacheTag property

Возвращает начальный тег «усы» для региона.

```csharp
public MustacheTag StartMustacheTag { get; }
```

### Примеры

Показывает, как работать с тегами усов.

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
* пространство имен [Aspose.Words.MailMerging](../../mailmergeregioninfo/)
* сборка [Aspose.Words](../../../)


