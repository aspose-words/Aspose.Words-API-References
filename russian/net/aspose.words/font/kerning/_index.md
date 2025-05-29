---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Kerning, контролируйте, когда начинается кернинг для оптимальной четкости текста и дизайна. Улучшите свою типографику с точностью!
type: docs
weight: 180
url: /ru/net/aspose.words/font/kerning/
---
## Font.Kerning property

Возвращает или задает размер шрифта, при котором начинается кернинг.

```csharp
public double Kerning { get; set; }
```

## Примеры

Показывает, как указать размер шрифта, при котором начинает действовать кернинг.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Установите размер шрифта конструктора и минимальный размер, при котором кернинг вступит в силу.
// Размер шрифта ниже порога кернинга, поэтому в следующем фрагменте кернинга не будет.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Установите порог кернинга так, чтобы текущий размер шрифта конструктора был выше него.
// Любой текст, который мы добавим с этого момента, будет иметь кернинг. Пробелы между символами
// будет скорректирован, что обычно приводит к более эстетически приятному тексту.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
