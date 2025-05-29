---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Shading, которое предоставляет объект Shading для настраиваемого форматирования шрифта, улучшая визуальную привлекательность вашего текста.
type: docs
weight: 330
url: /ru/net/aspose.words/font/shading/
---
## Font.Shading property

Возвращает[`Shading`](../../shading/) объект, который ссылается на форматирование штриховки для шрифта.

```csharp
public Shading Shading { get; }
```

## Примеры

Показывает, как применить затенение к тексту, созданному с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Один из способов сделать текст, созданный с использованием нашего белого цвета шрифта, видимым
// — применить эффект затенения фона.
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
