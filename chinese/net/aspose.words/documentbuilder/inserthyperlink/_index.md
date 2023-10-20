---
title: DocumentBuilder.InsertHyperlink
linktitle: InsertHyperlink
articleTitle: InsertHyperlink
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder InsertHyperlink 方法. 在文档中插入超链接 在 C#.
type: docs
weight: 360
url: /zh/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

在文档中插入超链接。

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| displayText | String | 要在文档中显示的链接的文本。 |
| urlOrBookmark | String | 链接目的地。可以是文档中的 url 或书签的名称。 此方法总是在 url 的开头和结尾添加撇号。 |
| isBookmark | Boolean | 如果前一个参数是文档内的书签名称，则为 true； false 是前一个参数是 URL。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)表示插入字段的对象。

## 评论

请注意，您需要使用显式 为超链接显示文本指定字体格式[`Font`](../font/)财产。

此方法在内部调用[`InsertField`](../insertfield/)在文档中插入一个 MS Word HYPERLINK field 。

## 例子

演示如何插入引用本地书签的超链接。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// 插入一个链接到书签的 HYPERLINK 字段。我们可以通过字段开关
// 将“InsertHyperlink”方法作为包含引用书签名称的参数的一部分。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

显示如何插入超链接字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// 插入一个超链接并用自定义格式强调它。
// 超链接将是一段可点击的文本，它将把我们带到 URL 中指定的位置。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + 左键单击 Microsoft Word 文本中的链接将通过新的 Web 浏览器窗口将我们带到 URL。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

展示如何使用文档构建器的格式化堆栈。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置字体格式，然后写入超链接之前的文本。
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// 在堆栈上保留我们当前的格式化配置。
builder.PushFont();

// 通过应用新样式来更改构建器的当前格式。
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// 恢复我们之前保存的字体格式并从堆栈中删除元素。
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
