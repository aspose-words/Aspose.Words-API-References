---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words для .NET
description: Откройте для себя свойство LayoutOptions ContinuousSectionPageNumberingRestart для бесшовного управления нумерацией страниц в непрерывных разделах. Оптимизируйте макет документа сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Возвращает или задает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Примечания

Значение по умолчанию:Always . Это соответствует поведению MS Word 2019, который был последней версией на момент введения этой опции. Более старая логика нумерации страниц, демонстрируемая MS Word 2016, доступна через эту опцию. Пожалуйста[`ContinuousSectionRestart`](../../continuoussectionrestart/) для описания поведения.

## Примеры

Показывает, как управлять нумерацией страниц в непрерывном разделе.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// По умолчанию поведение Aspose.Words соответствует Microsoft Word 2019.
// Если вам нужно старое поведение Aspose.Words, повторяющееся в Microsoft Word 2016, используйте 'ContinuousSectionRestart.FromNewPageOnly'.
// Нумерация страниц начинается заново только в том случае, если перед разделом на странице, с которого начинается раздел, нет другого контента,
// из-за этого нумерация будет сброшена на 2 со второй страницы.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Смотрите также

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
