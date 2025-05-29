---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font Shadow, улучшите свой текст с помощью стильных эффектов тени, чтобы придать вашим проектам поразительную визуальную привлекательность.
type: docs
weight: 340
url: /ru/net/aspose.words/font/shadow/
---
## Font.Shadow property

True, если шрифт отформатирован как затененный.

```csharp
public bool Shadow { get; set; }
```

## Примеры

Показывает, как создать фрагмент текста, отформатированный с тенью.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите флаг «Тень», чтобы применить эффект смещения тени,
// создавая впечатление, что буквы парят над страницей.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
