---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words LowCode ComparerContext class for efficient document comparison, enhancing your workflow with seamless integration and powerful features.
type: docs
weight: 4220
url: /net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

Document comparer context

```csharp
public class ComparerContext : ProcessorContext
```

## Constructors

| Name | Description |
| --- | --- |
| [ComparerContext](comparercontext/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | Indicates whether to accept revisions in the documents before comparing them. If the compared documents contain revisions and this flag is set to false, the processor will reject revisions. Default is `true`. |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | The author to be assigned to revisions created during document comparison. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | Options used upon comparing documents. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | The date and time assigned to revisions created during document comparison. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Font settings used by the processor. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Document layout options used by the processor. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Warning callback used by the processor. |

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

* class [ProcessorContext](../processorcontext/)
* namespace [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assembly [Aspose.Words](../../)
