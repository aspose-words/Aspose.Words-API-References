---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words for .NET
description: 了解如何有效地使用 Comparer Create 方法生成转换器处理器的新实例，以增强性能和效率。
type: docs
weight: 10
url: /zh/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

创建转换器处理器的新实例。

```csharp
public static Comparer Create()
```

### 也可以看看

* class [Comparer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

创建比较器处理器的新实例。

```csharp
public static Comparer Create(ComparerContext context)
```

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

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
