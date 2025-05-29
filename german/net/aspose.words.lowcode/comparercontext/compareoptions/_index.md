---
title: ComparerContext.CompareOptions
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die CompareOptions-Eigenschaft in ComparerContext, um den Dokumentvergleich mit leistungsstarken und flexiblen Optionen für genaue Ergebnisse zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.lowcode/comparercontext/compareoptions/
---
## ComparerContext.CompareOptions property

Beim Vergleichen von Dokumenten verwendete Optionen.

```csharp
public CompareOptions CompareOptions { get; }
```

## Beispiele

Zeigt, wie man Dokumente einfach anhand des Kontexts vergleicht.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente zu vergleichen:
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

Zeigt, wie Dokumente aus dem Stream mithilfe des Kontexts verglichen werden.

```csharp
// Es gibt mehrere Möglichkeiten, Dokumente aus dem Stream zu vergleichen:
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

### Siehe auch

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [ComparerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
