---
title: IReplacingCallback
second_title: Справочник по API Aspose.Words для .NET
description: Реализуйте этот интерфейс если вы хотите чтобы ваш собственный метод вызывался во время операции поиска и замены.
type: docs
weight: 4320
url: /ru/net/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface

Реализуйте этот интерфейс, если вы хотите, чтобы ваш собственный метод вызывался во время операции поиска и замены.

```csharp
public interface IReplacingCallback
```

## Методы

| Имя | Описание |
| --- | --- |
| [Replacing](../../aspose.words.replacing/ireplacingcallback/replacing)(ReplacingArgs) | Определяемый пользователем метод, который вызывается во время операции замены для каждого совпадения, найденного непосредственно перед выполнением замены. |

### Примеры

Показывает, как заменить все вхождения шаблона регулярного выражения другой строкой, отслеживая все такие замены.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Вставить документ после абзаца, содержащего совпадающий текст.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Удаляем абзац с совпадающим текстом.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Вставляет все узлы другого документа после абзаца или таблицы.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Пропустить узел, если это последний пустой абзац в разделе.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

Показывает, как отслеживать порядок обхода узлов операцией замены текста.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Вставить документ после абзаца, содержащего совпадающий текст.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Удаляем абзац с совпадающим текстом.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Вставляет все узлы другого документа после абзаца или таблицы.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Пропустить узел, если это последний пустой абзац в разделе.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

Показывает, как вставить все содержимое документа в качестве замены совпадения в операции поиска и замены.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Вставить документ после абзаца, содержащего совпадающий текст.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // Удаляем абзац с совпадающим текстом.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// Вставляет все узлы другого документа после абзаца или таблицы.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // Пропустить узел, если это последний пустой абзац в разделе.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### Смотрите также

* пространство имен [Aspose.Words.Replacing](../../aspose.words.replacing)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
