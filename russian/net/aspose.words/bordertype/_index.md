---
title: Enum BorderType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.BorderType перечисление. Определяет стороны границы.
type: docs
weight: 100
url: /ru/net/aspose.words/bordertype/
---
## BorderType enumeration

Определяет стороны границы.

Чтобы узнать больше, посетите[Программирование с документами](https://docs.aspose.com/words/net/programming-with-documents/) статья документации.

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
| Horizontal | `4` | Указывает горизонтальную границу между ячейками таблицы или между соответствующими абзацами. |
| Vertical | `5` | Определяет вертикальную границу между ячейками таблицы. |
| DiagonalDown | `6` | Определяет диагональную границу ячейки таблицы. |
| DiagonalUp | `7` | Определяет диагональную границу ячейки таблицы. |

### Примеры

Показывает, как вставить абзац с верхней границей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Устанавливаем ThemeColor только в том случае, если установлены LineWidth или LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


