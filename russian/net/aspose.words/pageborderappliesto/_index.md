---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.PageBorderAppliesTo для управления печатью границ страниц на определенных страницах для улучшенного форматирования документа.
type: docs
weight: 5070
url: /ru/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Указывает, на каких страницах печатается граница страницы.

```csharp
public enum PageBorderAppliesTo
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| AllPages | `0` | Граница страницы отображается на всех страницах раздела. |
| FirstPage | `1` | Граница страницы отображается только на первой странице раздела. |
| OtherPages | `2` | Граница страницы отображается на всех страницах, кроме первой страницы раздела. |

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
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
