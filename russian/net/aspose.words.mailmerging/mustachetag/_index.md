---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.MailMerging.MustacheTag — эффективно обрабатывайте теги «усы» для бесперебойной автоматизации документов и улучшенного слияния писем.
type: docs
weight: 4570
url: /ru/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

Представляет тег «усы».

```csharp
public class MustacheTag
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | Получает начальную позицию тега, отсчитываемую от нуля, от начала[`ReferenceRun`](./referencerun/) . |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | Получает прогон, содержащий начало тега. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | Получает текст тега. |

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

* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../)
