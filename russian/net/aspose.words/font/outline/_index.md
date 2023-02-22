---
title: Font.Outline
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Истинно если шрифт отформатирован как контурный.
type: docs
weight: 290
url: /ru/net/aspose.words/font/outline/
---
## Font.Outline property

Истинно, если шрифт отформатирован как контурный.

```csharp
public bool Outline { get; set; }
```

### Примеры

Показывает, как создать набор текста в формате структуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите флаг Outline, чтобы изменить цвет заливки текста на белый и
 // оставляем вокруг каждого символа тонкий контур исходного цвета текста.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


