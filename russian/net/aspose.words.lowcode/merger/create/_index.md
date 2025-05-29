---
title: Merger.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words для .NET
description: Откройте для себя метод Merger Create, позволяющий легко создать новый экземпляр процессора слияния почты для оптимизированной обработки документов и повышения эффективности.
type: docs
weight: 10
url: /ru/net/aspose.words.lowcode/merger/create/
---
## Create() {#create}

Создает новый экземпляр процессора слияния почты.

```csharp
public static Merger Create()
```

### Смотрите также

* class [Merger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)

---

## Create(*[MergerContext](../../mergercontext/)*) {#create_1}

Создает новый экземпляр процессора слияния почты.

```csharp
public static Merger Create(MergerContext context)
```

## Примеры

Показывает, как объединить документы в один выходной документ с использованием контекста.

```csharp
//Существует несколько способов объединения документов:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.1.docx")
    .Execute();

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1, firstLoadOptions)
    .From(inputDoc2, secondLoadOptions)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.2.docx", SaveFormat.Docx)
    .Execute();

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
    .From(inputDoc1)
    .From(inputDoc2)
    .To(ArtifactsDir + "LowCode.MergeContextDocuments.3.docx", saveOptions)
    .Execute();
```

Показывает, как объединить документы из потока в один выходной документ с использованием контекста.

```csharp
//Существует несколько способов объединения документов:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

using (FileStream firstStreamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Tables.docx", FileMode.Open, FileAccess.Read))
    {
        OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn)
            .From(secondStreamIn)
            .To(streamOut, saveOptions)
            .Execute();

        LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
        LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MergeStreamContextDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
            Merger.Create(new MergerContext() { MergeFormatMode = MergeFormatMode.KeepSourceFormatting })
            .From(firstStreamIn, firstLoadOptions)
            .From(secondStreamIn, secondLoadOptions)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
    }
}
```

### Смотрите также

* class [MergerContext](../../mergercontext/)
* class [Merger](../)
* пространство имен [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* сборка [Aspose.Words](../../../)
