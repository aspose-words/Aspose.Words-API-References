---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words for .NET
description: Discover how to effectively use the Comparer Create method to generate new instances of the converter processor for enhanced performance and efficiency.
type: docs
weight: 10
url: /net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

Creates new instance of the converter processor.

```csharp
public static Comparer Create()
```

### See Also

* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

Creates new instance of the comparer processor.

```csharp
public static Comparer Create(ComparerContext context)
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

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* namespace [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../../)
