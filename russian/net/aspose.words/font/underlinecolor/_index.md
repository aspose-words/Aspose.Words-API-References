---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font UnderlineColor, которое позволит легко настроить цвет подчеркивания шрифта для улучшения стиля текста и визуальной привлекательности.
type: docs
weight: 550
url: /ru/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Возвращает или задает цвет подчеркивания, применяемого к шрифту.

```csharp
public Color UnderlineColor { get; set; }
```

## Примеры

Показывает, как настроить стиль и цвет подчеркивания текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
