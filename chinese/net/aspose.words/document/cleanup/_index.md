---
title: Document.Cleanup
linktitle: Cleanup
articleTitle: Cleanup
second_title: 用于 .NET 的 Aspose.Words
description: Document Cleanup 方法. 从文档中清除未使用的样式和列表 在 C#.
type: docs
weight: 540
url: /zh/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

从文档中清除未使用的样式和列表。

```csharp
public void Cleanup()
```

## 例子

演示如何从文档中删除未使用的自定义样式。

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// 与内置样式相结合，文档现在有八种样式。
// 自定义样式在应用于文档的某些部分时算作“已使用”，
// 这意味着我们添加的四种样式当前未使用。
Assert.AreEqual(8, doc.Styles.Count);

// 应用自定义字符样式，然后应用自定义列表样式。这样做会将样式标记为“已使用”。
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Cleanup();

Assert.AreEqual(6, doc.Styles.Count);

// 删除应用了自定义样式的每个节点，再次将其标记为“未使用”。
// 再次运行 Cleanup 方法来删除它们。
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup();

Assert.AreEqual(4, doc.Styles.Count);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## Cleanup(*[CleanupOptions](../../cleanupoptions/)*) {#cleanup_1}

根据给定的条件从文档中清除未使用的样式和列表[`CleanupOptions`](../../cleanupoptions/).

```csharp
public void Cleanup(CleanupOptions options)
```

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

* class [CleanupOptions](../../cleanupoptions/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
