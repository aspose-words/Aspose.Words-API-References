---
title: Border.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Border Shadow, чтобы улучшить свой дизайн! Управляйте эффектами тени для границ и улучшите свой пользовательский интерфейс с помощью потрясающих визуальных эффектов.
type: docs
weight: 60
url: /ru/net/aspose.words/border/shadow/
---
## Border.Shadow property

Возвращает или задает значение, указывающее, имеет ли граница тень.

```csharp
public bool Shadow { get; set; }
```

## Примечания

В Microsoft Word, чтобы граница имела тень, границы со всех четырех сторон (слева, сверху, справа и снизу) должны быть одного типа, ширины, цвета и все должны иметь свойство Shadow, установленное на`истинный`.

## Примеры

Показывает, как создать зеленую волнистую рамку страницы с тенью.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### Смотрите также

* class [Border](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
