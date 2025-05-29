---
title: SplitOptions.SplitCriteria
linktitle: SplitCriteria
articleTitle: SplitCriteria
second_title: Aspose.Words для .NET
description: Узнайте, как свойство SplitOptions SplitCriteria улучшает управление документами, эффективно разделяя содержимое на управляемые разделы.
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/splitoptions/splitcriteria/
---
## SplitOptions.SplitCriteria property

Задает критерии разделения документа на части.

```csharp
public SplitCriteria SplitCriteria { get; set; }
```

## Примеры

Показывает, как разделить документ по страницам.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Смотрите также

* enum [SplitCriteria](../../splitcriteria/)
* class [SplitOptions](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
