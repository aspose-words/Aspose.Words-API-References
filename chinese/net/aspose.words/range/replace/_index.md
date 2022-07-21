---
title: Replace
second_title: Aspose.Words for .NET API 参考
description: 用替换字符串替换所有出现的指定字符串模式
type: docs
weight: 80
url: /zh/net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

用替换字符串替换所有出现的指定字符串模式。

```csharp
public int Replace(string pattern, string replacement)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern | String | 要替换的字符串。 |
| replacement | String | 替换所有出现的模式的字符串。 |

### 返回值

更换的次数。

### 评论

该模式不会用作正则表达式。 请使用[`Replace`](../replace)如果你需要正则表达式。

使用不区分大小写的比较。

方法能够处理模式和替换字符串中的中断。

如果你需要使用中断，你应该使用特殊的元字符：

* **&amp;p** - 段落中断
* **&amp;b** - 分节符
* **&amp;m** - 分页符
* **&amp;l** - 手动换行

使用方法[`Replace`](../replace)进行更灵活的定制。

### 例子

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// 在 Numbers 之后插入分节符。
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

演示如何对文档内容执行查找和替换文本操作。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// 对我们文档的内容执行查找和替换操作，并验证发生的替换次数。
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

演示如何为查找和替换操作找到匹配项的段落添加格式。

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

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“Alignment”属性设置为“ParagraphAlignment.Right”以使每个段落右对齐
// 包含查找和替换操作找到的匹配项。
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// 用感叹号替换段落分隔符之前的每个句号。
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### 也可以看看

* class [Range](../../range)
* 命名空间 [Aspose.Words](../../range)
* 部件 [Aspose.Words](../../../)

---

## Replace(Regex, string) {#replace_2}

用另一个字符串替换所有出现的由正则表达式指定的字符模式。

```csharp
public int Replace(Regex pattern, string replacement)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern | Regex | 用于查找匹配项的正则表达式模式。 |
| replacement | String | 替换所有出现的模式的字符串。 |

### 返回值

更换的次数。

### 评论

替换正则表达式捕获的整个匹配项。

方法能够处理模式和替换字符串中的中断。

如果你需要使用中断，你应该使用特殊的元字符：

* **&amp;p** - 段落中断
* **&amp;b** - 分节符
* **&amp;m** - 分页符
* **&amp;l** - 手动换行

使用方法[`Replace`](../replace)进行更灵活的定制。

### 例子

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// 用分节符替换每个数字。
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

展示如何用其他文本替换所有出现的正则表达式模式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### 也可以看看

* class [Range](../../range)
* 命名空间 [Aspose.Words](../../range)
* 部件 [Aspose.Words](../../../)

---

## Replace(string, string, FindReplaceOptions) {#replace_1}

用替换字符串替换所有出现的指定字符串模式。

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern | String | 要替换的字符串。 |
| replacement | String | 替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions)对象以指定其他选项。 |

### 返回值

更换的次数。

### 评论

该模式不会用作正则表达式。 请使用[`Replace`](../replace)如果你需要正则表达式。

方法能够处理模式和替换字符串中的中断。

如果你需要使用中断，你应该使用特殊的元字符：

* **&amp;p** - 段落中断
* **&amp;b** - 分节符
* **&amp;m** - 分页符
* **&amp;l** - 手动换行
* **&amp;&amp;** - ＆ 特点

### 例子

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// 在 Numbers 之后插入分节符。
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

显示如何替换文档页脚中的文本。

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

显示在执行查找和替换操作时如何切换区分大小写。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“MatchCase”标志设置为“true”以在查找要替换的字符串时应用区分大小写。
// 将“MatchCase”标志设置为“false”以在搜索要替换的文本时忽略字符大小写。
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

显示如何切换独立的纯字查找和替换操作。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“FindWholeWordsOnly”标志设置为“true”以替换找到的文本，如果它不是另一个词的一部分。
// 将“FindWholeWordsOnly”标志设置为“false”以替换所有文本，无论其周围环境如何。
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

演示如何替换表格和单元格中文本字符串的所有实例。

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

// 对整个表执行查找和替换操作。
table.Range.Replace("Carrots", "Eggs", options);

// 对表格最后一行的最后一个单元格执行查找和替换操作。
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* 命名空间 [Aspose.Words](../../range)
* 部件 [Aspose.Words](../../../)

---

## Replace(Regex, string, FindReplaceOptions) {#replace_3}

用另一个字符串替换所有出现的由正则表达式指定的字符模式。

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| pattern | Regex | 用于查找匹配项的正则表达式模式。 |
| replacement | String | 替换所有出现的模式的字符串。 |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions)对象以指定其他选项。 |

### 返回值

更换的次数。

### 评论

替换正则表达式捕获的整个匹配项。

方法能够处理模式和替换字符串中的中断。

如果你需要使用中断，你应该使用特殊的元字符：

* **&amp;p** - 段落中断
* **&amp;b** - 分节符
* **&amp;m** - 分页符
* **&amp;l** - 手动换行
* **&amp;&amp;** - ＆ 特点

### 例子

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// 用分节符替换每个数字。
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

展示如何用另一个字符串替换所有出现的正则表达式模式，同时跟踪所有此类替换。

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
    FindReplaceOptions options = new FindReplaceOptions();

    // 设置一个回调来跟踪“替换”方法将进行的任何替换。
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// 维护由查找和替换操作完成的每个文本替换的日志
/// 并注意原始匹配文本的值。
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

演示如何在查找和替换操作中插入整个文档的内容以替换匹配项。

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // 在包含匹配文本的段落之后插入一个文档。
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // 删除匹配文本的段落。
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// 在段落或表格之后插入另一个文档的所有节点。
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
                // 如果节点是节中的最后一个空段落，则跳过该节点。
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

### 也可以看看

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions)
* class [Range](../../range)
* 命名空间 [Aspose.Words](../../range)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
