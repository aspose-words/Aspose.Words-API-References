---
title: MustacheTag.ReferenceRun
linktitle: ReferenceRun
articleTitle: ReferenceRun
second_title: Aspose.Words для .NET
description: Откройте для себя MustacheTag ReferenceRun. Получите доступ к запуску, который отмечает начало вашего тега, для бесперебойного управления данными и повышения производительности.
type: docs
weight: 20
url: /ru/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Получает прогон, содержащий начало тега.

```csharp
public Run ReferenceRun { get; }
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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
