---
title: Splitter.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words per .NET
description: Scopri come creare in modo efficiente una nuova istanza del processore splitter con la nostra guida semplice da seguire per un'integrazione perfetta e prestazioni migliorate.
type: docs
weight: 10
url: /it/net/aspose.words.lowcode/splitter/create/
---
## Splitter.Create method

Crea una nuova istanza del processore splitter.

```csharp
public static Splitter Create(SplitterContext context)
```

## Esempi

Mostra come dividere un documento in pagine utilizzando il contesto.

```csharp
string doc = MyDir + "Big document.docx";

SplitterContext splitterContext = new SplitterContext();
splitterContext.SplitOptions.SplitCriteria = SplitCriteria.Page;

Splitter.Create(splitterContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.SplitContextDocument.docx")
    .Execute();
```

Mostra come suddividere un documento dal flusso in base alle pagine, utilizzando il contesto.

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

### Guarda anche

* class [SplitterContext](../../splittercontext/)
* class [Splitter](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
