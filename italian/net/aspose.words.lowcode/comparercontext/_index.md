---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words LowCode ComparerContext per un confronto efficiente dei documenti, migliorando il tuo flusso di lavoro con un'integrazione perfetta e potenti funzionalità.
type: docs
weight: 4220
url: /it/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

Contesto comparatore documenti

```csharp
public class ComparerContext : ProcessorContext
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ComparerContext](comparercontext/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | Indica se accettare le revisioni nei documenti prima di confrontarli. Se i documenti confrontati contengono revisioni e questo flag è impostato su falso, il processore rifiuterà le revisioni. Il valore predefinito è`VERO` . |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | L'autore da assegnare alle revisioni create durante il confronto dei documenti. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | Opzioni utilizzate durante il confronto dei documenti. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | Data e ora assegnate alle revisioni create durante il confronto dei documenti. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Impostazioni del font utilizzate dal processore. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opzioni di layout del documento utilizzate dal processore. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Callback di avviso utilizzato dal processore. |

## Esempi

Mostra come confrontare in modo semplice i documenti utilizzando il contesto.

```csharp
// Esistono diversi modi per confrontare i documenti:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

ComparerContext comparerContext = new ComparerContext();
comparerContext.CompareOptions.IgnoreCaseChanges = true;
comparerContext.Author = "Author";
comparerContext.DateTime = new DateTime();

Comparer.Create(comparerContext)
    .From(firstDoc)
    .From(secondDoc)
    .To(ArtifactsDir + "LowCode.CompareContextDocuments.docx")
    .Execute();
```

Mostra come confrontare i documenti dal flusso utilizzando il contesto.

```csharp
// Esistono diversi modi per confrontare i documenti dal flusso:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        ComparerContext comparerContext = new ComparerContext();
        comparerContext.CompareOptions.IgnoreCaseChanges = true;
        comparerContext.Author = "Author";
        comparerContext.DateTime = new DateTime();

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareContextStreamDocuments.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Create(comparerContext)
                .From(firstStreamIn)
                .From(secondStreamIn)
                .To(streamOut, SaveFormat.Docx)
                .Execute();
    }
}
```

### Guarda anche

* class [ProcessorContext](../processorcontext/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
