---
title: SplitterContext.SplitOptions
linktitle: SplitOptions
articleTitle: SplitOptions
second_title: Aspose.Words per .NET
description: Scopri come ottimizzare la gestione dei documenti con la proprietà SplitOptions di SplitterContext per una suddivisione efficiente e flessibile dei contenuti. Migliora il tuo flusso di lavoro oggi stesso.
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/splittercontext/splitoptions/
---
## SplitterContext.SplitOptions property

Opzioni di divisione del documento.

```csharp
public SplitOptions SplitOptions { get; }
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

* class [SplitOptions](../../splitoptions/)
* class [SplitterContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
