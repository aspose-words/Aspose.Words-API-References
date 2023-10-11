---
title: DocumentBuilder.InsertHyperlink
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将超链接插入到文档中
type: docs
weight: 370
url: /zh/net/aspose.words/documentbuilder/inserthyperlink/
---
## DocumentBuilder.InsertHyperlink method

将超链接插入到文档中。

```csharp
public Field InsertHyperlink(string displayText, string urlOrBookmark, bool isBookmark)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| displayText | String | 要在文档中显示的链接文本。 |
| urlOrBookmark | String | 链接目的地。可以是文档中的 url 或书签名称。 此方法始终在 url 的开头和结尾添加撇号。 |
| isBookmark | Boolean | `真的`如果前一个参数是文档内书签的名称； `错误的`前面的参数是一个URL。 |

### 返回值

A[`Field`](../../../aspose.words.fields/field/)代表插入字段的对象。

### 评论

请注意，您需要使用以下命令明确指定超链接显示文本的字体格式 [`Font`](../font/)财产。

该方法内部调用[`InsertField`](../insertfield/)将 MS Word HYPERLINK field 插入文档中。

### 例子

演示如何插入引用本地书签的超链接。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartBookmark("Bookmark1");
builder.Write("Bookmarked text. ");
builder.EndBookmark("Bookmark1");
builder.Writeln("Text outside of the bookmark.");

// 插入链接到书签的 HYPERLINK 字段。我们可以通过现场开关
// 作为包含引用书签名称的参数的一部分发送到“InsertHyperlink”方法。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Link to Bookmark1", @"Bookmark1"" \o ""Hyperlink Tip", true);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlinkToLocalBookmark.docx");
```

演示如何插入超链接字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// 插入超链接并使用自定义格式强调它。
// 超链接将是一段可点击的文本，它将带我们到 URL 中指定的位置。
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + 左键单击 Microsoft Word 中文本中的链接将通过新的 Web 浏览器窗口转到 URL。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

演示如何使用文档生成器的格式堆栈。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 设置字体格式，然后编写超链接之前的文本。
builder.Font.Name = "Arial";
builder.Font.Size = 24;
builder.Write("To visit Google, hold Ctrl and click ");

// 在堆栈上保留当前的格式配置。
builder.PushFont();

// 通过应用新样式来更改构建器的当前格式。
builder.Font.StyleIdentifier = StyleIdentifier.Hyperlink;
builder.InsertHyperlink("here", "http://www.google.com", false);

Assert.AreEqual(Color.Blue.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.Single, builder.Font.Underline);

// 恢复我们之前保存的字体格式并从堆栈中删除该元素。
builder.PopFont();

Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());
Assert.AreEqual(Underline.None, builder.Font.Underline);

builder.Write(". We hope you enjoyed the example.");

doc.Save(ArtifactsDir + "DocumentBuilder.PushPopFont.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


