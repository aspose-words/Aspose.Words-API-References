---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words для .NET
description: Узнайте, как управлять настройками приоритета стилей, чтобы оптимизировать сортировку стилей на панели задач. Улучшите свой рабочий процесс с помощью эффективной организации стилей!
type: docs
weight: 160
url: /ru/net/aspose.words/style/priority/
---
## Style.Priority property

Возвращает/задает целочисленное значение, представляющее приоритет сортировки стилей на панели задач «Стили».

```csharp
public int Priority { get; set; }
```

## Примеры

Показывает, как расставить приоритеты и скрыть стиль.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### Смотрите также

* class [Style](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
