---
title: ComparerContext.CompareOptions
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CompareOptions i ComparerContext för att förbättra dokumentjämförelsen med kraftfulla och flexibla alternativ för korrekta resultat.
type: docs
weight: 40
url: /sv/net/aspose.words.lowcode/comparercontext/compareoptions/
---
## ComparerContext.CompareOptions property

Alternativ som används vid jämförelse av dokument.

```csharp
public CompareOptions CompareOptions { get; }
```

## Exempel

Visar hur man enkelt jämför dokument med hjälp av kontext.

```csharp
// Det finns flera sätt att jämföra dokument:
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

Visar hur man jämför dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att jämföra dokument från strömmen:
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

### Se även

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [ComparerContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
