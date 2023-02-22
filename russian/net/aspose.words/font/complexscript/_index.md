---
title: Font.ComplexScript
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Указывает должно ли содержимое этого запуска рассматриваться как сложный текст сценария независимо от их значений символов Unicode при определении форматирования для этого запуска.
type: docs
weight: 80
url: /ru/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Указывает, должно ли содержимое этого запуска рассматриваться как сложный текст сценария независимо от их значений символов Unicode при определении форматирования для этого запуска.

```csharp
public bool ComplexScript { get; set; }
```

### Примеры

Показывает, как добавить текст, который всегда рассматривается как сложный сценарий.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


