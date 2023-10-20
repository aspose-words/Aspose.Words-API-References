---
title: DocumentBuilder.PopFont
linktitle: PopFont
articleTitle: PopFont
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder PopFont 方法. 检索先前保存在堆栈中的字符格式 在 C#.
type: docs
weight: 590
url: /zh/net/aspose.words/documentbuilder/popfont/
---
## DocumentBuilder.PopFont method

检索先前保存在堆栈中的字符格式。

```csharp
public void PopFont()
```

## 例子

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

* property [Font](../font/)
* method [PushFont](../pushfont/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
