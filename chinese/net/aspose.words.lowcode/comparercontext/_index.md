---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words LowCode ComparerContext 类，实现高效的文档比较，通过无缝集成和强大的功能增强您的工作流程。
type: docs
weight: 4220
url: /zh/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

文档比较器上下文

```csharp
public class ComparerContext : ProcessorContext
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ComparerContext](comparercontext/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | 指示在比较文档之前是否接受文档中的修订。 如果比较的文档包含修订，并且此标志设置为 false，则处理器将拒绝修订。 默认值为`真的`. |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | 文档比较期间创建的修订的指定作者。 |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | 比较文档时使用的选项。 |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | 文档比较期间创建的修订的日期和时间。 |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | 处理器使用的字体设置。 |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | 处理器使用的文档布局选项。 |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | 处理器使用的警告回调。 |

## 例子

展示如何使用上下文简单地比较文档。

```csharp
// 有几种方法可以比较文档：
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

展示如何使用上下文比较流中的文档。

```csharp
// 有几种方法可以比较流中的文档：
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

### 也可以看看

* class [ProcessorContext](../processorcontext/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
