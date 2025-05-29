---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font ComplexScript, гарантирующее, что ваш текст будет отформатирован как сложный шрифт для улучшения читаемости и стиля, независимо от значений Unicode.
type: docs
weight: 80
url: /ru/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Указывает, будет ли содержимое этого прогона рассматриваться как сложный текст сценария независимо от их значений символов Unicode при определении форматирования для этого прогона.

```csharp
public bool ComplexScript { get; set; }
```

## Примеры

Показывает, как добавить текст, который всегда рассматривается как сложный шрифт.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
