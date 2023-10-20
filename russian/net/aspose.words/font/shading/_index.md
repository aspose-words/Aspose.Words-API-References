---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words для .NET
description: Font Shading свойство. ВозвращаетShading объект который относится к форматированию затенения для шрифта на С#.
type: docs
weight: 320
url: /ru/net/aspose.words/font/shading/
---
## Font.Shading property

Возвращает[`Shading`](../../shading/) объект, который относится к форматированию затенения для шрифта.

```csharp
public Shading Shading { get; }
```

## Примеры

Показывает, как применить затенение к тексту, созданному с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Один из способов сделать текст, созданный с использованием белого цвета шрифта, видимым
// заключается в применении эффекта затенения фона.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### Смотрите также

* class [Shading](../../shading/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
