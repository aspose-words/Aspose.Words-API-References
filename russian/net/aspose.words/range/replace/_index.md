---
title: Replace
second_title: Справочник по API Aspose.Words для .NET
description: Заменяет все вхождения указанного шаблона строки символов заменяющей строкой.
type: docs
weight: 80
url: /ru/net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

Заменяет все вхождения указанного шаблона строки символов заменяющей строкой.

```csharp
public int Replace(string pattern, string replacement)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | String | Строка для замены. |
| replacement | String | Строка для замены всех вхождений шаблона. |

### Возвращаемое значение

Количество произведенных замен.

### Примечания

Шаблон не будет использоваться как регулярное выражение. Пожалуйста, используйте[`Replace`](../replace)если вам нужны регулярные выражения.

Используется сравнение без учета регистра.

Метод может обрабатывать разрывы как в шаблоне, так и в замещающих строках.

При работе с разрывами следует использовать специальные метасимволы:

* **&amp;p** - разрыв абзаца
* **&amp;b** - разрыв раздела
* **&amp;m** - разрыв страницы
* **&amp;l** - разрыв строки вручную

Использовать метод[`Replace`](../replace)иметь более гибкую настройку.

### Примеры

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для свойства "Выравнивание" значение "ParagraphAlignment.Right", чтобы выровнять каждый абзац по правому краю.
// который содержит совпадение, найденное операцией поиска и замены.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Замените каждую точку перед разрывом абзаца восклицательным знаком.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

Показывает, как выполнить операцию поиска и замены текста в содержимом документа .

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для свойства "Выравнивание" значение "ParagraphAlignment.Right", чтобы выровнять каждый абзац по правому краю.
// который содержит совпадение, найденное операцией поиска и замены.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Замените каждую точку перед разрывом абзаца восклицательным знаком.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

Показывает, как добавить форматирование к абзацам, в которых операция поиска и замены обнаружила совпадения.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для свойства "Выравнивание" значение "ParagraphAlignment.Right", чтобы выровнять каждый абзац по правому краю.
// который содержит совпадение, найденное операцией поиска и замены.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// Замените каждую точку перед разрывом абзаца восклицательным знаком.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### Смотрите также

* class [Range](../../range)
* пространство имен [Aspose.Words](../../range)
* сборка [Aspose.Words](../../../)

---

## Replace(Regex, string) {#replace_2}

Заменяет все вхождения шаблона символов, заданного регулярным выражением, другой строкой.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |

### Возвращаемое значение

Количество произведенных замен.

### Примечания

Заменяет все совпадение, захваченное регулярным выражением.

Метод может обрабатывать разрывы как в шаблоне, так и в замещающих строках.

При работе с разрывами следует использовать специальные метасимволы:

* **&amp;p** - разрыв абзаца
* **&amp;b** - разрыв раздела
* **&amp;m** - разрыв страницы
* **&amp;l** - разрыв строки вручную

Использовать метод[`Replace`](../replace)для более гибкой настройки.

### Примеры

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

Показывает, как заменить все вхождения шаблона регулярного выражения другим текстом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### Смотрите также

* class [Range](../../range)
* пространство имен [Aspose.Words](../../range)
* сборка [Aspose.Words](../../../)

---

## Replace(string, string, FindReplaceOptions) {#replace_1}

Заменяет все вхождения указанного шаблона строки символов заменяющей строкой.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| шаблон | String | Строка для замены. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions)объект для указания дополнительных параметров. |

### Возвращаемое значение

Количество произведенных замен.

### Примечания

Шаблон не будет использоваться как регулярное выражение. Пожалуйста, используйте[`Replace`](../replace)если вам нужно обычные выражения.

Метод может обрабатывать разрывы как в шаблоне, так и в замещающих строках.

При работе с разрывами следует использовать специальные метасимволы:

* **&amp;p** - разрыв абзаца
* **&amp;b** - разрыв раздела
* **&amp;m** - разрыв страницы
* **&amp;l** - разрыв строки вручную
* **&amp;&amp;** - &amp; символ

### Примеры

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

 // Выполнить операцию поиска и замены для всей таблицы.
table.Range.Replace("Carrots", "Eggs", options);

 // Выполняем операцию поиска и замены в последней ячейке последней строки таблицы.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

Показывает, как заменить текст в нижнем колонтитуле документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

 // Выполнить операцию поиска и замены для всей таблицы.
table.Range.Replace("Carrots", "Eggs", options);

 // Выполняем операцию поиска и замены в последней ячейке последней строки таблицы.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

Показывает, как переключить чувствительность к регистру при выполнении операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

 // Выполнить операцию поиска и замены для всей таблицы.
table.Range.Replace("Carrots", "Eggs", options);

 // Выполняем операцию поиска и замены в последней ячейке последней строки таблицы.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

Показывает, как переключать автономные операции поиска и замены только для слов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

 // Выполнить операцию поиска и замены для всей таблицы.
table.Range.Replace("Carrots", "Eggs", options);

 // Выполняем операцию поиска и замены в последней ячейке последней строки таблицы.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

Показывает, как заменить все экземпляры строки текста в таблице и ячейке.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

 // Выполнить операцию поиска и замены для всей таблицы.
table.Range.Replace("Carrots", "Eggs", options);

 // Выполняем операцию поиска и замены в последней ячейке последней строки таблицы.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* пространство имен [Aspose.Words](../../range)
* сборка [Aspose.Words](../../../)

---

## Replace(Regex, string, FindReplaceOptions) {#replace_3}

Заменяет все вхождения шаблона символов, заданного регулярным выражением, другой строкой.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| шаблон | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions)объект для указания дополнительных параметров. |

### Возвращаемое значение

Количество произведенных замен.

### Примечания

Заменяет все совпадение, захваченное регулярным выражением.

Метод может обрабатывать разрывы как в шаблоне, так и в замещающих строках.

При работе с разрывами следует использовать специальные метасимволы:

* **&amp;p** - разрыв абзаца
* **&amp;b** - разрыв раздела
* **&amp;m** - разрыв страницы
* **&amp;l** - разрыв строки вручную
* **&amp;&amp;** - &amp; символ

### Примеры

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

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* пространство имен [Aspose.Words](../../range)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
