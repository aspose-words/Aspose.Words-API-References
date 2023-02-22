---
title: Document.UpdateWordCount
second_title: Aspose.Words for .NET API 参考
description: Document 方法. 更新文档的字数统计属性
type: docs
weight: 770
url: /zh/net/aspose.words/document/updatewordcount/
---
## UpdateWordCount() {#updatewordcount}

更新文档的字数统计属性。

```csharp
public void UpdateWordCount()
```

### 评论

**更新字数**重新计算和更新 Characters、Words 和 Paragraphs 中的属性[`BuiltInDocumentProperties`](../builtindocumentproperties/)的集合 **文档**.

注意 **更新字数**不更新行数和页数属性。 使用`UpdateWordCount`重载并将 True 值作为参数传递来执行此操作。

当您使用评估版时，评估水印也将包含在字数中 。

### 例子

显示如何更新文档中的所有列表标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words 不会实时跟踪此类文档指标。
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// 要获得其中三个属性的准确值，我们需要手动更新它们。
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// 对于行数，我们需要调用更新方法的特定重载。
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)

---

## UpdateWordCount(bool) {#updatewordcount_1}

更新文档的字数统计属性，可选择更新[`Lines`](../../../aspose.words.properties/builtindocumentproperties/lines/)属性.

```csharp
public void UpdateWordCount(bool updateLinesCount)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| updateLinesCount | Boolean | 如果应计算文档中的行数，则为真。 |

### 评论

此方法将重建文档的页面布局。

### 例子

显示如何更新文档中的所有列表标签。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words 不会实时跟踪此类文档指标。
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// 要获得其中三个属性的准确值，我们需要手动更新它们。
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// 对于行数，我们需要调用更新方法的特定重载。
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

### 也可以看看

* class [Document](../)
* 命名空间 [Aspose.Words](../../document/)
* 部件 [Aspose.Words](../../../)


