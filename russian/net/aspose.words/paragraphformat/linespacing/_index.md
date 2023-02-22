---
title: ParagraphFormat.LineSpacing
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает межстрочный интервал в пунктах для абзаца.
type: docs
weight: 180
url: /ru/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

Получает или задает межстрочный интервал (в пунктах) для абзаца.

```csharp
public double LineSpacing { get; set; }
```

### Примечания

Когда для свойства LineSpacingRule установлено значение AtLeast, межстрочный интервал может быть больше или равен , но не меньше указанного значения LineSpacing.

Когда для свойства LineSpacingRule задано значение Exactly, междустрочный интервал никогда не изменяется с на указанное значение LineSpacing, даже если внутри абзаца используется более крупный шрифт.

### Примеры

Показывает, как работать с межстрочным интервалом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены три правила межстрочного интервала, которые мы можем определить с помощью
// свойство абзаца "LineSpacingRule" для настройки интервала между абзацами.
// 1 - Установить минимальное расстояние.
// Это даст вертикальный отступ для строк текста любого размера
// это слишком мало, чтобы поддерживать минимальную высоту строки.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - Установить точный интервал.
// Использование размеров шрифта, которые слишком велики для интервала, приведет к обрезанию текста.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - Установите интервал как кратный межстрочному интервалу по умолчанию, который по умолчанию составляет 12 пунктов.
// Этот тип интервала будет масштабироваться для разных размеров шрифта.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


