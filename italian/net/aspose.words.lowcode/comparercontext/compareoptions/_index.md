---
title: ComparerContext.CompareOptions
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words per .NET
description: Scopri la proprietà CompareOptions in ComparerContext per migliorare il confronto dei documenti con opzioni potenti e flessibili per risultati accurati.
type: docs
weight: 40
url: /it/net/aspose.words.lowcode/comparercontext/compareoptions/
---
## ComparerContext.CompareOptions property

Opzioni utilizzate durante il confronto dei documenti.

```csharp
public CompareOptions CompareOptions { get; }
```

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

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [ComparerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
