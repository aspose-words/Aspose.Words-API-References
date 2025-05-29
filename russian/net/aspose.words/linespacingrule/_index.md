---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.LineSpacingRule для настраиваемого интервала между строками абзаца. Улучшите форматирование документа с точным контролем и улучшенной читаемостью.
type: docs
weight: 3890
url: /ru/net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

Задает значения межстрочного интервала для абзаца.

```csharp
public enum LineSpacingRule
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| AtLeast | `0` | Межстрочный интервал может быть больше или равен, но не меньше, значения, указанного в[`LineSpacing`](../paragraphformat/linespacing/) свойство. |
| Exactly | `1` | Межстрочный интервал никогда не изменяется от значения, указанного в the [`LineSpacing`](../paragraphformat/linespacing/) свойство, даже если внутри абзаца используется более крупный шрифт. |
| Multiple | `2` | Межстрочный интервал указан в[`LineSpacing`](../paragraphformat/linespacing/) Свойство как количество линий. Одна линия равна 12 точкам. |

## Примеры

Показывает, как работать с межстрочным интервалом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три правила межстрочного интервала, которые мы можем определить с помощью
// свойство абзаца "LineSpacingRule" для настройки интервала между абзацами.
// 1 — Установить минимальный интервал.
// Это даст вертикальный отступ строкам текста любого размера
// это слишком мало для поддержания минимальной высоты строки.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Установить точный интервал.
// Использование шрифта слишком большого размера для данного интервала приведет к обрезанию текста.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Установить интервал как кратный межстрочному интервалу по умолчанию, который по умолчанию составляет 12 пунктов.
// Этот тип интервала будет масштабироваться под разные размеры шрифта.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
