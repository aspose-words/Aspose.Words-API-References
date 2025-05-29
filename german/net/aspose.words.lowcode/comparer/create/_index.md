---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die Comparer Create-Methode effektiv nutzen können, um neue Instanzen des Konverterprozessors für verbesserte Leistung und Effizienz zu generieren.
type: docs
weight: 10
url: /de/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

Erstellt eine neue Instanz des Konverterprozessors.

```csharp
public static Comparer Create()
```

### Siehe auch

* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

Erstellt eine neue Instanz des Vergleichsprozessors.

```csharp
public static Comparer Create(ComparerContext context)
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

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
