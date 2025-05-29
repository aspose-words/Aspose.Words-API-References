---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SemiHidden управляет видимостью стилей в галерее стилей и на панели задач, улучшая рабочий процесс и эффективность дизайна.
type: docs
weight: 170
url: /ru/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

Возвращает/задает, будет ли стиль скрыт из галереи стилей и из панели задач «Стили».

```csharp
public bool SemiHidden { get; set; }
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
