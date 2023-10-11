---
title: Font.TextEffect
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Получает или задает эффект анимации шрифта.
type: docs
weight: 450
url: /ru/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Получает или задает эффект анимации шрифта.

```csharp
public TextEffect TextEffect { get; set; }
```

### Примеры

Показывает, как применить визуальный эффект к бегу.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Старые версии Microsoft Word поддерживают только эффекты анимации шрифтов.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Смотрите также

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


