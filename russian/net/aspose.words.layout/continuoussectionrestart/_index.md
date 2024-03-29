---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words для .NET
description: Aspose.Words.Layout.ContinuousSectionRestart перечисление. Представляет различное поведение при вычислении номеров страниц в непрерывном разделе который перезапускает нумерацию страниц на С#.
type: docs
weight: 3300
url: /ru/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Представляет различное поведение при вычислении номеров страниц в непрерывном разделе, который перезапускает нумерацию страниц.

```csharp
public enum ContinuousSectionRestart
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Always | `0` | Нумерация страниц всегда начинается заново независимо от потока содержимого. |
| FromNewPageOnly | `1` | Нумерация страниц возобновляется только в том случае, если перед разделом на странице, где этот раздел начинается, нет другого содержимого. |

## Примеры

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

* пространство имен [Aspose.Words.Layout](../../aspose.words.layout/)
* сборка [Aspose.Words](../../)
