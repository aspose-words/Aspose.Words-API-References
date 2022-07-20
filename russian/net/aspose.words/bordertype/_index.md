---
title: BorderType
second_title: Справочник по API Aspose.Words для .NET
description: Определяет стороны границы.
type: docs
weight: 90
url: /ru/net/aspose.words/bordertype/
---
## BorderType enumeration

Определяет стороны границы.

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
| Horizontal | `4` | Указывает горизонтальную границу между ячейками в таблице или между соответствующими абзацами. |
| Vertical | `5` | Указывает вертикальную границу между ячейками в таблице. |
| DiagonalDown | `6` | Указывает диагональную границу в ячейке таблицы. |
| DiagonalUp | `7` | Указывает диагональную границу в ячейке таблицы. |

### Примеры

Показывает, как вставить абзац с верхней границей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->