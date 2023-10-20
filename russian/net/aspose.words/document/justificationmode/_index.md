---
title: Document.JustificationMode
linktitle: JustificationMode
articleTitle: JustificationMode
second_title: Aspose.Words для .NET
description: Document JustificationMode свойство. Получает или задает настройку межсимвольного интервала в документе на С#.
type: docs
weight: 230
url: /ru/net/aspose.words/document/justificationmode/
---
## Document.JustificationMode property

Получает или задает настройку межсимвольного интервала в документе.

```csharp
public JustificationMode JustificationMode { get; set; }
```

## Примеры

Показывает, как управлять интервалом между символами.

```csharp
Document doc = new Document(MyDir + "Document.docx");

JustificationMode justificationMode = doc.JustificationMode;
if (justificationMode == JustificationMode.Expand)                
    doc.JustificationMode = JustificationMode.Compress;

doc.Save(ArtifactsDir + "Document.SetJustificationMode.docx");
```

### Смотрите также

* enum [JustificationMode](../../../aspose.words.settings/justificationmode/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
