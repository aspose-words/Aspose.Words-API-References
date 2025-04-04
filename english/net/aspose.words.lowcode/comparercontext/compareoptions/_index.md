---
title: ComparerContext.CompareOptions
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words for .NET
description: Discover the CompareOptions property in ComparerContext to enhance document comparison with powerful and flexible options for accurate results.
type: docs
weight: 40
url: /net/aspose.words.lowcode/comparercontext/compareoptions/
---
## ComparerContext.CompareOptions property

Options used upon comparing documents.

```csharp
public CompareOptions CompareOptions { get; }
```

## Examples

Shows how to simple compare documents using context.

```csharp
// There is a several ways to compare documents:
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

Shows how to compare documents from the stream using context.

```csharp
// There is a several ways to compare documents from the stream:
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

### See Also

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [ComparerContext](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
