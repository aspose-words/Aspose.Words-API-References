---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words per .NET
description: Scopri come utilizzare in modo efficace il metodo Comparer Create per generare nuove istanze del processore del convertitore per ottenere prestazioni ed efficienza migliorate.
type: docs
weight: 10
url: /it/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

Crea una nuova istanza del processore del convertitore.

```csharp
public static Comparer Create()
```

### Guarda anche

* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

Crea una nuova istanza del processore di confronto.

```csharp
public static Comparer Create(ComparerContext context)
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

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
