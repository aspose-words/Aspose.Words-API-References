---
title: MustacheTag.Text
second_title: Справочник по API Aspose.Words для .NET
description: MustacheTag свойство. Получает текст тега.
type: docs
weight: 30
url: /ru/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Получает текст тега.

```csharp
public string Text { get; }
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

* class [MustacheTag](../)
* пространство имен [Aspose.Words.MailMerging](../../mustachetag/)
* сборка [Aspose.Words](../../../)


