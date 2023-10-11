---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
second_title: Справочник по API Aspose.Words для .NET
description: LayoutOptions свойство. Получает или задает режим поведения для вычисления номеров страниц когда непрерывный раздел перезапускает нумерацию страниц.
type: docs
weight: 40
url: /ru/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Получает или задает режим поведения для вычисления номеров страниц, когда непрерывный раздел перезапускает нумерацию страниц.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

### Примечания

Значение по умолчанию:Always. Он соответствует поведению MS Word 2019, который был последней версией на момент введения этой опции. С помощью этой опции доступна более старая логика нумерации страниц, продемонстрированная MS Word 2016. Пожалуйста[`ContinuousSectionRestart`](../../continuoussectionrestart/) для описания поведения.

### Примеры

Показывает, как управлять нумерацией страниц в непрерывном разделе.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// По умолчанию поведение Aspose.Words соответствует Microsoft Word 2019.
// Если вам нужно старое поведение Aspose.Words, повторяющееся Microsoft Word 2016, используйте ContinousSectionRestart.FromNewPageOnly.
// Нумерация страниц возобновляется только в том случае, если перед разделом на странице, где начинается раздел, нет другого контента,
// из-за этого нумерация будет сброшена на 2 со второй страницы.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Смотрите также

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* пространство имен [Aspose.Words.Layout](../../layoutoptions/)
* сборка [Aspose.Words](../../../)


