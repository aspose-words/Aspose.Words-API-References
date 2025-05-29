---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Outline. Легко форматируйте шрифты как контуры для уникального дизайнерского штриха. Улучшите свою типографику с помощью этой простой функции!
type: docs
weight: 300
url: /ru/net/aspose.words/font/outline/
---
## Font.Outline property

True, если шрифт отформатирован как контурный.

```csharp
public bool Outline { get; set; }
```

## Примеры

Показывает, как создать фрагмент текста, отформатированный в виде структуры.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите флаг Outline, чтобы изменить цвет заливки текста на белый и
 // оставьте тонкий контур вокруг каждого символа в исходном цвете текста.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
