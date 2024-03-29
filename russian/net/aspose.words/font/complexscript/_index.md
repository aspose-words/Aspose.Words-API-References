---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words для .NET
description: Font ComplexScript свойство. Указывает должно ли содержимое этого запуска рассматриваться как сложный текст сценария независимо от значений символов Юникода при определении форматирования для этого запуска на С#.
type: docs
weight: 80
url: /ru/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Указывает, должно ли содержимое этого запуска рассматриваться как сложный текст сценария независимо от значений символов Юникода при определении форматирования для этого запуска.

```csharp
public bool ComplexScript { get; set; }
```

## Примеры

Показывает, как добавить текст, который всегда рассматривается как сложный скрипт.

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
