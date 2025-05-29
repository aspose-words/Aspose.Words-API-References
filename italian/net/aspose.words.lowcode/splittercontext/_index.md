---
title: SplitterContext Class
linktitle: SplitterContext
articleTitle: SplitterContext
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.LowCode.SplitterContext per una suddivisione efficiente dei documenti, migliorando il flusso di lavoro con un'integrazione perfetta e funzionalità potenti.
type: docs
weight: 4430
url: /it/net/aspose.words.lowcode/splittercontext/
---
## SplitterContext class

Contesto di divisione del documento.

```csharp
public class SplitterContext : ProcessorContext
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [SplitterContext](splittercontext/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Impostazioni del font utilizzate dal processore. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opzioni di layout del documento utilizzate dal processore. |
| [SplitOptions](../../aspose.words.lowcode/splittercontext/splitoptions/) { get; } | Opzioni di divisione del documento. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Callback di avviso utilizzato dal processore. |

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

* class [ProcessorContext](../processorcontext/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
