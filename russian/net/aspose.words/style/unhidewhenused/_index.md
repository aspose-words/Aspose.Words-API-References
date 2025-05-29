---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words для .NET
description: Узнайте, как управлять свойством UnhideWhenUsed для стилей. Управляйте видимостью в галерее стилей и панели задач, чтобы улучшить дизайн вашего документа.
type: docs
weight: 210
url: /ru/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

Возвращает/задает, отображается ли стиль, используемый в текущем документе, из галереи стилей и из панели задач «Стили». True, когда используемый стиль должен отображаться в галерее стилей.

```csharp
public bool UnhideWhenUsed { get; set; }
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
