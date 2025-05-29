---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words для .NET
description: Исследуйте перечисление Aspose.Words.Layout.ContinuousSectionRestart для гибких вариантов нумерации страниц в непрерывных разделах. Улучшайте макет документа без усилий!
type: docs
weight: 3750
url: /ru/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Представляет различные варианты поведения при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц.

```csharp
public enum ContinuousSectionRestart
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Always | `0` | Нумерация страниц всегда начинается заново независимо от потока контента. |
| FromNewPageOnly | `1` | Нумерация страниц начинается заново только в том случае, если перед разделом на странице, с которой начинается раздел, нет другого контента. |

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

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
