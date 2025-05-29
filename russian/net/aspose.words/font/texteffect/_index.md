---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font TextEffect, позволяющее легко настраивать анимацию шрифтов и дополнять свои проекты динамическими текстовыми эффектами, создавая захватывающий пользовательский опыт.
type: docs
weight: 460
url: /ru/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Получает или задает эффект анимации шрифта.

```csharp
public TextEffect TextEffect { get; set; }
```

## Примеры

Показывает, как применить визуальный эффект к прогону.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
