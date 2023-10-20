---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words для .NET
description: Font Shadow свойство. True если шрифт отформатирован как затененный на С#.
type: docs
weight: 330
url: /ru/net/aspose.words/font/shadow/
---
## Font.Shadow property

True, если шрифт отформатирован как затененный.

```csharp
public bool Shadow { get; set; }
```

## Примеры

Показывает, как создать фрагмент текста, отформатированный с помощью тени.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите флаг Shadow, чтобы применить эффект смещения тени,
// создаем впечатление, будто буквы плавают над страницей.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
