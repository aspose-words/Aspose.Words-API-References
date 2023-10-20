---
title: CleanupOptions Class
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.CleanupOptions 班级. 允许指定文档清理选项 在 C#.
type: docs
weight: 210
url: /zh/net/aspose.words/cleanupoptions/
---
## CleanupOptions class

允许指定文档清理选项。

要了解更多信息，请访问[清理文档](https://docs.aspose.com/words/net/clean-up-a-document/)文档文章。

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
| [DuplicateStyle](../../aspose.words/cleanupoptions/duplicatestyle/) { get; set; } | 获取/设置一个标志，指示是否应从文档中删除重复样式。 默认值为`错误的`. |
| [UnusedBuiltinStyles](../../aspose.words/cleanupoptions/unusedbuiltinstyles/) { get; set; } | 指定未使用[`BuiltIn`](../style/builtin/)应从文档中删除样式。 |
| [UnusedLists](../../aspose.words/cleanupoptions/unusedlists/) { get; set; } | 指定是否应从文档中删除未使用的列表和列表定义。 默认值为`真的`. |
| [UnusedStyles](../../aspose.words/cleanupoptions/unusedstyles/) { get; set; } | 指定是否应从文档中删除未使用的样式。 默认值为`真的`. |

## 例子

演示如何从文档中删除所有未使用的自定义样式。

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// 与内置样式相结合，文档现在有八种样式。
// 当文档中存在任何文本时，自定义样式被标记为“已使用”
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
// 当使用 CleanupOptions 对象配置 Cleanup() 方法时，它可以定位未使用的样式并删除它们。
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // 删除应用了自定义样式的每个节点，再次将其标记为“未使用”。
// 重新运行 Cleanup 方法来删除它们。
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
