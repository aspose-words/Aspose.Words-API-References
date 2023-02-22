---
title: Font.Kerning
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Получает или задает размер шрифта с которого начинается кернинг.
type: docs
weight: 180
url: /ru/net/aspose.words/font/kerning/
---
## Font.Kerning property

Получает или задает размер шрифта, с которого начинается кернинг.

```csharp
public double Kerning { get; set; }
```

### Примеры

Показывает, как указать размер шрифта, при котором кернинг начинает действовать.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Установите размер шрифта построителя и минимальный размер, при котором кернинг вступит в силу.
// Размер шрифта падает ниже порога кернинга, поэтому в приведенном ниже примере кернинга не будет.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Установить порог кернинга так, чтобы текущий размер шрифта построителя был выше него.
// К любому тексту, который мы добавим с этой точки, будет применен кернинг. Пробелы между символами
// будет скорректировано, что обычно приводит к несколько более эстетичному прогону текста.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


