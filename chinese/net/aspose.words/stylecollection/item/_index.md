---
title: StyleCollection.Item
second_title: Aspose.Words for .NET API 参考
description: StyleCollection 财产. 通过名称或别名获取样式
type: docs
weight: 50
url: /zh/net/aspose.words/stylecollection/item/
---
## StyleCollection indexer (1 of 3)

通过名称或别名获取样式。

```csharp
public Style this[string name] { get; }
```

### 评论

区分大小写，返回`无效的`如果未找到给定名称的样式。

如果这是尚不存在的内置样式的英文名称，则会自动创建它。

### 例子

显示何时重新计算文档的页面布局。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// 第一次将文档保存为 PDF、图像或打印
// 在其页面中缓存文档的布局。
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// 以某种方式修改文档。
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // 在当前版本的Aspose.Words中，修改文档不会自动重建
// 缓存的页面布局。如果我们希望缓存布局
// 为了保持最新状态，我们需要手动更新它。
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

### 也可以看看

* class [Style](../../style/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../stylecollection/)
* 部件 [Aspose.Words](../../../)

---

## StyleCollection indexer (2 of 3)

通过其区域设置独立标识符获取内置样式。

```csharp
public Style this[StyleIdentifier sti] { get; }
```

| 范围 | 描述 |
| --- | --- |
| sti | A[`StyleIdentifier`](../../styleidentifier/)指定要检索的内置样式的值。 |

### 评论

当访问尚不存在的样式时，会自动创建它。

### 例子

演示如何将样式添加到文档的样式集合中。

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// 为我们稍后可能添加到此集合中的新样式设置默认参数。
styles.DefaultFont.Name = "Courier New";
// 如果我们添加“StyleType.Paragraph”的样式，集合将应用以下值
// 将其“DefaultParagraphFormat”属性设置为样式的“ParagraphFormat”属性。
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// 添加样式，然后验证它是否具有默认设置。
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### 也可以看看

* class [Style](../../style/)
* enum [StyleIdentifier](../../styleidentifier/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../stylecollection/)
* 部件 [Aspose.Words](../../../)

---

## StyleCollection indexer (3 of 3)

通过索引获取样式。

```csharp
public Style this[int index] { get; }
```

### 例子

演示如何将样式添加到文档的样式集合中。

```csharp
Document doc = new Document();

StyleCollection styles = doc.Styles;
// 为我们稍后可能添加到此集合中的新样式设置默认参数。
styles.DefaultFont.Name = "Courier New";
// 如果我们添加“StyleType.Paragraph”的样式，集合将应用以下值
// 将其“DefaultParagraphFormat”属性设置为样式的“ParagraphFormat”属性。
styles.DefaultParagraphFormat.FirstLineIndent = 15.0;
// 添加样式，然后验证它是否具有默认设置。
styles.Add(StyleType.Paragraph, "MyStyle");

Assert.AreEqual("Courier New", styles[4].Font.Name);
Assert.AreEqual(15.0, styles["MyStyle"].ParagraphFormat.FirstLineIndent);
```

### 也可以看看

* class [Style](../../style/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../stylecollection/)
* 部件 [Aspose.Words](../../../)


