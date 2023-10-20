---
title: Range.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words для .NET
description: Range Replace метод. Заменяет все вхождения указанного шаблона строки символов заменяющей строкой на С#.
type: docs
weight: 90
url: /ru/net/aspose.words/range/replace/
---
## Replace(*string, string*) {#replace}

Заменяет все вхождения указанного шаблона строки символов заменяющей строкой.

```csharp
public int Replace(string pattern, string replacement)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | String | Строка, которую необходимо заменить. |
| replacement | String | Строка для замены всех вхождений шаблона. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Шаблон не будет использоваться в качестве регулярного выражения. Пожалуйста, используйте`Replace`если вам нужны регулярные выражения.

Используется сравнение без учета регистра.

Метод способен обрабатывать разрывы как в шаблонах, так и в строках замены.

Если вам нужно работать с разрывами, следует использовать специальные метасимволы:

* **&amp;п** - разрыв абзаца
* **&amp;б** - разрыв раздела
* **&amp;м** - разрыв страницы
* **&amp;л** - ручной разрыв строки

Использовать метод`Replace` чтобы иметь более гибкую настройку.

## Примеры

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Вставляет разрыв абзаца после Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Показывает, как выполнить операцию поиска и замены текста в содержимом документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// Выполняем операцию поиска и замены содержимого нашего документа и проверяем количество произошедших замен.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
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

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для свойства «Alignment» значение «ParagraphAlignment.Right», чтобы выровнять каждый абзац по правому краю.
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

* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Replace(*Regex, string*) {#replace_2}

Заменяет все вхождения шаблона символов, указанного в регулярном выражении, другой строкой.

```csharp
public int Replace(Regex pattern, string replacement)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Заменяет все совпадение, полученное регулярным выражением.

Метод способен обрабатывать разрывы как в шаблонах, так и в строках замены.

Если вам нужно работать с разрывами, следует использовать специальные метасимволы:

* **&amp;п** - разрыв абзаца
* **&amp;б** - разрыв раздела
* **&amp;м** - разрыв страницы
* **&amp;л** - ручной разрыв строки

Использовать метод`Replace` чтобы иметь более гибкую настройку.

## Примеры

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Заменяет каждое число разрывом абзаца.
doc.Range.Replace(new Regex(@"\d+"), "&p");
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

* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Replace(*string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

Заменяет все вхождения указанного шаблона строки символов заменяющей строкой.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | String | Строка, которую необходимо заменить. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект, чтобы указать дополнительные параметры. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Шаблон не будет использоваться в качестве регулярного выражения. Пожалуйста, используйте`Replace`если вам нужны регулярные выражения.

Метод способен обрабатывать разрывы как в шаблонах, так и в строках замены.

Если вам нужно работать с разрывами, следует использовать специальные метасимволы:

* **&amp;п** - разрыв абзаца
* **&amp;б** - разрыв раздела
* **&amp;м** - разрыв страницы
* **&amp;л** - ручной разрыв строки
* **&amp;&amp;** - &amp; характер

## Примеры

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// Вставляет разрыв абзаца после Numbers.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

Показывает, как заменить текст в нижнем колонтитуле документа.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Показывает, как переключить чувствительность к регистру при выполнении операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для флага «MatchCase» значение «true», чтобы применять чувствительность к регистру при поиске заменяемых строк.
// Установите флаг «MatchCase» в значение «false», чтобы игнорировать регистр символов при поиске текста для замены.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Показывает, как переключать отдельные операции поиска и замены только по словам.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг «FindWholeWordsOnly» в значение «true», чтобы заменить найденный текст, если он не является частью другого слова.
// Установите для флага «FindWholeWordsOnly» значение «false», чтобы заменить весь текст независимо от его окружения.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

Показывает, как заменить все экземпляры String текста в таблице и ячейке.

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

// Выполняем операцию поиска и замены для всей таблицы.
table.Range.Replace("Carrots", "Eggs", options);

// Выполняем операцию поиска и замены последней ячейки последней строки таблицы.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)

---

## Replace(*Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

Заменяет все вхождения шаблона символов, указанного в регулярном выражении, другой строкой.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | Regex | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | String | Строка для замены всех вхождений шаблона. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) объект, чтобы указать дополнительные параметры. |

### Возвращаемое значение

Количество произведенных замен.

## Примечания

Заменяет все совпадение, полученное регулярным выражением.

Метод способен обрабатывать разрывы как в шаблонах, так и в строках замены.

Если вам нужно работать с разрывами, следует использовать специальные метасимволы:

* **&amp;п** - разрыв абзаца
* **&amp;б** - разрыв раздела
* **&amp;м** - разрыв страницы
* **&amp;л** - ручной разрыв строки
* **&amp;&amp;** - &amp; характер

## Примеры

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// Заменяет каждое число разрывом абзаца.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

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

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
