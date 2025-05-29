---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.BorderType для настраиваемых параметров границ. Улучшите свои документы с помощью точного управления границами и стиля!
type: docs
weight: 290
url: /ru/net/aspose.words/bordertype/
---
## BorderType enumeration

Указывает стороны границы.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) документальная статья.

```csharp
public enum BorderType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `-1` | Значение по умолчанию. |
| Bottom | `0` | Указывает нижнюю границу абзаца или ячейки таблицы. |
| Left | `1` | Указывает левую границу абзаца или ячейки таблицы. |
| Right | `2` | Указывает правую границу абзаца или ячейки таблицы. |
| Top | `3` | Указывает верхнюю границу абзаца или ячейки таблицы. |
| Horizontal | `4` | Задает горизонтальную границу между ячейками в таблице или между соответствующими абзацами. |
| Vertical | `5` | Задает вертикальную границу между ячейками в таблице. |
| DiagonalDown | `6` | Задает диагональную границу в ячейке таблицы. |
| DiagonalUp | `7` | Задает диагональную границу в ячейке таблицы. |

## Примеры

Показывает, как вставить абзац с верхней границей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Устанавливайте ThemeColor только при установке LineWidth или LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
