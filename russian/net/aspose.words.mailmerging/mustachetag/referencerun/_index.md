---
title: MustacheTag.ReferenceRun
second_title: Справочник по API Aspose.Words для .NET
description: MustacheTag свойство. Получает серию содержащую начало тега.
type: docs
weight: 20
url: /ru/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Получает серию, содержащую начало тега.

```csharp
public Run ReferenceRun { get; }
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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* пространство имен [Aspose.Words.MailMerging](../../mustachetag/)
* сборка [Aspose.Words](../../../)


