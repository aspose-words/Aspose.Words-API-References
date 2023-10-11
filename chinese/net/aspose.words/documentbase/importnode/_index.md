---
title: DocumentBase.ImportNode
second_title: Aspose.Words for .NET API 参考
description: DocumentBase 方法. 将节点从另一个文档导入到当前文档
type: docs
weight: 100
url: /zh/net/aspose.words/documentbase/importnode/
---
## ImportNode(Node, bool) {#importnode}

将节点从另一个文档导入到当前文档。

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | Node | 正在导入的节点。 |
| isImportChildren | Boolean | `真的`递归导入所有子节点；否则，`错误的`。 |

### 返回值

属于当前文档的克隆节点。

### 评论

该方法使用UseDestinationStyles解决格式问题的选项。

导入节点会创建属于导入文档的源节点的副本。 返回的节点没有父节点。源节点不会从原始文档中更改或删除。

在将另一个文档中的节点插入到此文档中之前，必须将其导入。 在导入期间，特定于文档的属性（例如对样式和列表的引用）将从原始文档翻译 到导入文档。导入节点后，可以使用将其插入 到文档中的适当位置Node)或 Node)。

如果源节点已经属于目标文档，则只需创建源节点的深层clone 。

### 例子

演示如何将节点从一个文档导入到另一个文档。

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// 每个节点都有一个父文档，即包含该节点的文档。
// 将节点插入到不属于该节点的文档中将会抛出异常。
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// 使用 ImportNode 方法创建节点的副本，其中将包含文档
// 调用 ImportNode 方法并将其设置为新的所有者文档。
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// 我们现在可以将节点插入到文档中。
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### 也可以看看

* class [Node](../../node/)
* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../documentbase/)
* 部件 [Aspose.Words](../../../)

---

## ImportNode(Node, bool, ImportFormatMode) {#importnode_1}

将节点从另一个文档导入到当前文档，并提供控制格式的选项。

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| srcNode | Node | 要导入的节点。 |
| isImportChildren | Boolean | `真的`递归导入所有子节点；否则，`错误的`。 |
| importFormatMode | ImportFormatMode | 指定如何合并冲突的样式格式。 |

### 返回值

克隆的导入节点。该节点属于目标文档，但没有父节点。

### 评论

此重载对于控制样式和列表格式的导入方式很有用。

导入节点会创建属于导入文档的源节点的副本。 返回的节点没有父节点。源节点不会从原始文档中更改或删除。

在将另一个文档中的节点插入到此文档中之前，必须将其导入。 在导入期间，特定于文档的属性（例如对样式和列表的引用）将从原始文档翻译 到导入文档。导入节点后，可以使用将其插入 到文档中的适当位置Node)或 Node)。

如果源节点已经属于目标文档，则只需创建源节点的深层clone 。

### 例子

演示如何使用特定选项将节点从源文档导入到目标文档。

```csharp
// 创建两个文档并为每个文档添加字符样式。
// 将样式配置为具有相同的名称，但文本格式不同。
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// 将目标文档中的Section导入到源文档中，导致样式名称冲突。
// 如果我们使用目标样式，则导入的源文本具有相同的样式名称
// 作为目标文本将采用目标样式。
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// 如果我们使用 ImportFormatMode.KeepDifferentStyles，则保留源样式，
// 命名冲突可以通过添加后缀来解决。
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### 也可以看看

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* 命名空间 [Aspose.Words](../../documentbase/)
* 部件 [Aspose.Words](../../../)


