---
title: Class CleanupOptions
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.CleanupOptions 班级. 允许指定文档清理选项
type: docs
weight: 200
url: /zh/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

允许指定文档清理选项。

```csharp
public class CleanupOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [CleanupOptions](cleanupoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | 获取/设置一个标志，指示是否应从文档中删除重复样式。 默认值为 **错误的**. |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | 指定未使用的[`BuiltIn`](../style/builtin/)样式应从 document. 中删除 |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | 指定是否应从文档中删除未使用的列表和列表定义。 默认值为 **真的**. |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | 指定是否应从文档中删除未使用的样式。 默认值为 **真的**. |

### 例子

展示如何从文档中删除所有未使用的自定义样式。

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// 结合内置样式，文档现在有八种样式。
// 当文档中有任何文本时，自定义样式被标记为“已使用”
// 以该样式格式化。这意味着我们添加的 4 种样式当前未使用。
Assert.AreEqual(8, doc.Styles.Count);

// 应用自定义字符样式，然后应用自定义列表样式。这样做会将它们标记为“已使用”。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// 现在，有一种未使用的字符样式和一种未使用的列表样式。
// Cleanup() 方法，当配置了 CleanupOptions 对象时，可以针对未使用的样式并删除它们。
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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


