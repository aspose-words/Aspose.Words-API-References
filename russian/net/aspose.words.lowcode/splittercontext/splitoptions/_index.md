---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: Aspose.Words для .NET
description: Узнайте, как оптимизировать управление документами с помощью свойства SplitOptions SplitterContext для эффективного и гибкого разделения контента. Улучшите свой рабочий процесс сегодня.
type: docs
weight: 20
url: /ru/net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

Параметры разделения документа.

```csharp
public SplitOptions SplitOptions { get; }
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

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
