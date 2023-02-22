---
title: Interface IReplacingCallback
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Replacing.IReplacingCallback интерфейс. Реализуйте этот интерфейс если вы хотите чтобы ваш собственный метод вызывался во время операции поиска и замены.
type: docs
weight: 4370
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
| [Replacing](../../aspose.words.replacing/ireplacingcallback/replacing/)(ReplacingArgs) | Определенный пользователем метод, который вызывается во время операции замены для каждого совпадения, найденного непосредственно перед выполнением замены. |

### Примеры

Показывает, как заменить все вхождения шаблона регулярного выражения другой строкой, отслеживая все такие замены.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
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
/// Ведет журнал каждой замены текста, выполненной операцией поиска и замены
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

Показывает, как отслеживать порядок, в котором операция замены текста проходит через узлы.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
        {
            Document doc = new Document(MyDir + "Header and footer types.docx");

            Section firstPageSection = doc.FirstSection;

            ReplaceLog logger = new ReplaceLog();
            FindReplaceOptions options = new FindReplaceOptions { ReplacingCallback = logger };

            // Использование другого верхнего/нижнего колонтитула для первой страницы повлияет на порядок поиска.
            firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
            doc.Range.Replace(new Regex("(header|footer)"), "", options);

#if NET48 || NET5_0_OR_GREATER || JAVA
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
                    logger.Text.Replace("\r", ""));
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
                    logger.Text.Replace("\r", ""));
#elif __MOBILE__
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", logger.Text);
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", logger.Text);
#endif
        }

        /// <summary>
        /// Во время операции поиска и замены записывает содержимое каждого узла с текстом, который операция «находит»,
        /// в том состоянии, в котором он находился перед заменой.
        /// Это отобразит порядок, в котором операция замены текста проходит через узлы.
        /// </summary>
        private class ReplaceLog : IReplacingCallback
        {
            public ReplaceAction Replacing(ReplacingArgs args)
            {
                mTextBuilder.AppendLine(args.MatchNode.GetText());
                return ReplaceAction.Skip;
            }

            internal string Text => mTextBuilder.ToString();

            private readonly StringBuilder mTextBuilder = new StringBuilder();
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

* пространство имен [Aspose.Words.Replacing](../../aspose.words.replacing/)
* сборка [Aspose.Words](../../)


