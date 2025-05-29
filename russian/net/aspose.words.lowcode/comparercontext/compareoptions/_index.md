---
title: ComparerContext.CompareOptions
linktitle: CompareOptions
articleTitle: CompareOptions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство CompareOptions в ComparerContext, которое расширяет возможности сравнения документов с помощью эффективных и гибких опций для получения точных результатов.
type: docs
weight: 40
url: /ru/net/aspose.words.lowcode/comparercontext/compareoptions/
---
## ComparerContext.CompareOptions property

Параметры, используемые при сравнении документов.

```csharp
public CompareOptions CompareOptions { get; }
```

## Примеры

Показывает, как просто сравнивать документы, используя контекст.

```csharp
// Существует несколько способов сравнения документов:
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

Показывает, как сравнивать документы из потока, используя контекст.

```csharp
// Существует несколько способов сравнения документов из потока:
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

### Смотрите также

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [ComparerContext](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
