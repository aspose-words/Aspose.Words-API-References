---
title: Comparer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words для .NET
description: Узнайте, как эффективно использовать метод Comparer Create для создания новых экземпляров процессора преобразователя для повышения производительности и эффективности.
type: docs
weight: 10
url: /ru/net/aspose.words.lowcode/comparer/create/
---
## Create() {#create}

Создает новый экземпляр процессора преобразователя.

```csharp
public static Comparer Create()
```

### Смотрите также

* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Create(*[ComparerContext](../../comparercontext/)*) {#create_1}

Создает новый экземпляр процессора сравнения.

```csharp
public static Comparer Create(ComparerContext context)
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

* class [ComparerContext](../../comparercontext/)
* class [Comparer](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
