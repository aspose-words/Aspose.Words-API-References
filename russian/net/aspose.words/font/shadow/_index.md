---
title: Font.Shadow
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. True если шрифт отформатирован как затененный.
type: docs
weight: 330
url: /ru/net/aspose.words/font/shadow/
---
## Font.Shadow property

True, если шрифт отформатирован как затененный.

```csharp
public bool Shadow { get; set; }
```

### Примеры

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
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


