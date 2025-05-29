---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Spacing, чтобы легко настроить интервал между символами в пунктах. Улучшите читаемость и дизайн с помощью точного типографского контроля.
type: docs
weight: 390
url: /ru/net/aspose.words/font/spacing/
---
## Font.Spacing property

Возвращает или задает интервал (в пунктах) между символами .

```csharp
public double Spacing { get; set; }
```

## Примеры

Показывает, как задать горизонтальное масштабирование и интервалы для символов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте фрагмент текста и увеличьте ширину символов до 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Добавьте фрагмент текста и добавьте 1 пункт дополнительного горизонтального интервала между каждым символом.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Добавьте фрагмент текста и сблизьте символы на 1 пункт.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
