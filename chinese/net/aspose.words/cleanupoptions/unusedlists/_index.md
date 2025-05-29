---
title: CleanupOptions.UnusedLists
linktitle: UnusedLists
articleTitle: UnusedLists
second_title: Aspose.Words for .NET
description: 使用 CleanupOptions 的 UnusedLists 属性优化您的文档。轻松移除未使用的列表和定义，打造更整洁、更高效的工作空间。
type: docs
weight: 40
url: /zh/net/aspose.words/cleanupoptions/unusedlists/
---
## CleanupOptions.UnusedLists property

指定是否应从文档中删除未使用的列表和列表定义。 默认值为`真的`.

```csharp
public bool UnusedLists { get; set; }
```

## 例子

展示如何从文档中删除所有未使用的自定义样式。

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// 结合内置样式，文档现在有八种样式。
// 当文档中存在任何文本时，自定义样式将被标记为“已使用”
// 格式化为该样式。这意味着我们添加的 4 种样式目前尚未使用。
Assert.AreEqual(8, doc.Styles.Count);

// 应用自定义字符样式，然后应用自定义列表样式。这样做会将它们标记为“已使用”。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// 现在，有一个未使用的字符样式和一个未使用的列表样式。
// 当使用 CleanupOptions 对象进行配置时，Cleanup() 方法可以定位未使用的样式并将其删除。
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // 删除应用自定义样式的每个节点，再次将其标记为“未使用”。
// 重新运行 Cleanup 方法以删除它们。
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### 也可以看看

* class [CleanupOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
