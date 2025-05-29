---
title: CleanupOptions.DuplicateStyle
linktitle: DuplicateStyle
articleTitle: DuplicateStyle
second_title: Aspose.Words for .NET
description: 使用 CleanupOptions 的 DuplicateStyle 属性优化您的文档——轻松移除重复样式，实现更简洁、更高效的格式。默认值为 false。
type: docs
weight: 20
url: /zh/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

获取/设置一个标志，指示是否应从文档中删除重复的样式。 默认值为`错误的`.

```csharp
public bool DuplicateStyle { get; set; }
```

## 例子

展示如何从文档中删除重复的样式。

```csharp
Document doc = new Document();

// 向文档添加两个具有相同属性的样式，
// 但名称不同。第二种样式被视为第一种样式的重复。
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// 将两种样式应用于文档内的不同段落。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// 配置一个 CleanOptions 对象，然后调用 Cleanup 方法替换所有重复的样式
// 与原始文档进行比较并从文档中删除重复项。
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### 也可以看看

* class [CleanupOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
