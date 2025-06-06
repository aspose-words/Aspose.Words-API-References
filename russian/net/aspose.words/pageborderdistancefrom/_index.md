---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
articleTitle: PageBorderDistanceFrom
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PageBorderDistanceFrom для точного размещения границ страницы. Улучшите форматирование документа с оптимальным позиционированием полей.
type: docs
weight: 5080
url: /ru/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

Задает положение границы страницы относительно поля страницы.

```csharp
public enum PageBorderDistanceFrom
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Text | `0` | Положение границы измеряется от края страницы. |
| PageEdge | `1` | Положение границы измеряется от края страницы. |

## Примеры

Показывает, как создать широкую синюю полосу в верхней части первой страницы.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Смотрите также

* class [PageSetup](../pagesetup/)
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
