---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words для .NET
description: Font Kerning свойство. Получает или задает размер шрифта с которого начинается кернинг на С#.
type: docs
weight: 180
url: /ru/net/aspose.words/font/kerning/
---
## Font.Kerning property

Получает или задает размер шрифта, с которого начинается кернинг.

```csharp
public double Kerning { get; set; }
```

## Примеры

Показывает, как указать размер шрифта, при котором кернинг начинает действовать.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Установите размер шрифта компоновщика и минимальный размер, при котором кернинг вступит в силу.
// Размер шрифта падает ниже порога кернинга, поэтому в приведенном ниже фрагменте кернинга не будет.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Установите порог кернинга так, чтобы текущий размер шрифта компоновщика был выше него.
// К любому тексту, который мы добавляем с этой точки, будет применен кернинг. Пробелы между символами
// будет скорректирован, что обычно приводит к более эстетичному воспроизведению текста.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
