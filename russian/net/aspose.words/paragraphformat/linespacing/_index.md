---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words для .NET
description: Легко настройте межстрочный интервал в абзацах с помощью свойства ParagraphFormat LineSpacing. Улучшите читаемость и стиль ваших документов!
type: docs
weight: 190
url: /ru/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Возвращает или задает межстрочный интервал (в пунктах) для абзаца.

```csharp
public double LineSpacing { get; set; }
```

## Примечания

Когда[`LineSpacingRule`](../linespacingrule/) свойство установлено наAtLeast , межстрочный интервал может быть больше или равен , но не меньше указанного`LineSpacing` ценить.

Когда[`LineSpacingRule`](../linespacingrule/) свойство установлено наExactly , межстрочный интервал никогда не меняется от указанного`LineSpacing` значение, даже если внутри абзаца используется более крупный шрифт.

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

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
