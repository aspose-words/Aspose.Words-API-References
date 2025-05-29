---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words для .NET
description: Узнайте, как эффективно создать новый экземпляр процессора-разделителя с помощью нашего простого руководства для бесшовной интеграции и повышения производительности.
type: docs
weight: 10
url: /ru/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

Создает новый экземпляр процессора-разделителя.

```csharp
public static Splitter Create(SplitterContext context)
```

## Примеры

Показывает, как разделить документ по страницам, используя контекст.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Показывает, как разделить документ из потока по страницам, используя контекст.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitterContext splitterContext = new SplitterContext();
    splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

    List<Stream> pages = new List<Stream>();
    Splitter.Create(splitterContext)
        .From(streamIn)
        .To(pages, SaveFormat.Docx)
        .Execute();
}
```

### Смотрите также

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
