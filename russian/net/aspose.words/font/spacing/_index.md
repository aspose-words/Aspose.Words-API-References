---
title: Font.Spacing
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Возвращает или устанавливает интервал в пунктах между символами .
type: docs
weight: 380
url: /ru/net/aspose.words/font/spacing/
---
## Font.Spacing property

Возвращает или устанавливает интервал (в пунктах) между символами .

```csharp
public double Spacing { get; set; }
```

### Примеры

Показывает, как установить горизонтальное масштабирование и интервал для символов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавляем фрагмент текста и увеличиваем ширину символа до 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Добавляем фрагмент текста и добавляем дополнительный горизонтальный интервал в 1 пт между каждым символом.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Добавляем фрагмент текста и сближаем символы на 1 пт.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


