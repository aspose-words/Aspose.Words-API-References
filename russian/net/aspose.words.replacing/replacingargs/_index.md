---
title: Class ReplacingArgs
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Replacing.ReplacingArgs сорт. Предоставляет данные для пользовательской операции замены.
type: docs
weight: 4650
url: /ru/net/aspose.words.replacing/replacingargs/
---
## ReplacingArgs class

Предоставляет данные для пользовательской операции замены.

Чтобы узнать больше, посетите[Найти и заменить](https://docs.aspose.com/words/net/find-and-replace/) статья документации.

```csharp
public class ReplacingArgs
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [GroupIndex](../../aspose.words.replacing/replacingargs/groupindex/) { get; set; } | Идентифицирует по индексу захваченную группу в[`Match`](./match/) , который необходимо заменить на[`Replacement`](./replacement/) строка. |
| [GroupName](../../aspose.words.replacing/replacingargs/groupname/) { get; set; } | Идентифицирует по имени захваченную группу в[`Match`](./match/) , который необходимо заменить на[`Replacement`](./replacement/) строка. |
| [Match](../../aspose.words.replacing/replacingargs/match/) { get; } | Match в результате одного совпадения выражения Regular во время **Заменять** . |
| [MatchNode](../../aspose.words.replacing/replacingargs/matchnode/) { get; } | Получает узел, содержащий начало совпадения. |
| [MatchOffset](../../aspose.words.replacing/replacingargs/matchoffset/) { get; } | Получает начальную позицию совпадения с отсчетом от нуля от начала узла, содержащего начало совпадения. |
| [Replacement](../../aspose.words.replacing/replacingargs/replacement/) { get; set; } | Получает или задает строку замены. |

### Примеры

Показывает, как заменить все вхождения шаблона регулярного выражения другой строкой, отслеживая при этом все такие замены.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();

    // Установите обратный вызов, который отслеживает любые замены, которые сделает метод "Replace".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// Ведёт журнал каждой замены текста, выполненной операцией поиска и замены
/// и отмечает значение исходного совпавшего текста.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

Показывает, как вставить содержимое всего документа в качестве замены совпадения в операции поиска и замены.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // Вставляем документ после абзаца, содержащего совпадающий текст.
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
                // Пропускаем узел, если это последний пустой абзац в разделе.
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

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* пространство имен [Aspose.Words.Replacing](../../aspose.words.replacing/)
* сборка [Aspose.Words](../../)


