---
title: StyleCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words for .NET
description: 使用 StyleCollection 的 AddCopy 方法轻松复制样式。立即增强您的设计工作流程，简化样式管理！
type: docs
weight: 70
url: /zh/net/aspose.words/stylecollection/addcopy/
---
## StyleCollection.AddCopy method

将样式复制到此集合中。

```csharp
public Style AddCopy(Style style)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| style | Style | 要复制的样式。 |

### 返回值

已复制样式，可供使用。

## 评论

要复制的样式可以属于同一文档，也可以属于不同的文档。

链接样式被复制。

此方法不会复制基本样式。

如果集合中已经包含同名样式，则新名称将自动生成，并添加从 0 开始的“_number”后缀，例如“Normal_0”、“Heading 1_1”等。使用[`Name`](../../style/name/)用于更改导入样式的名称的设置器。

## 例子

展示如何将样式从一个文档导入到另一个文档。

```csharp
Document srcDoc = new Document();

// 为源文档创建自定义样式。
Style srcStyle = srcDoc.Styles.Add(StyleType.Paragraph, "MyStyle");
srcStyle.Font.Color = Color.Red;

// 将源文档的自定义样式导入目标文档。
Document dstDoc = new Document();
Style newStyle = dstDoc.Styles.AddCopy(srcStyle);

// 导入的样式与其源样式的外观相同。
Assert.AreEqual("MyStyle", newStyle.Name);
Assert.AreEqual(Color.Red.ToArgb(), newStyle.Font.Color.ToArgb());
```

展示如何克隆文档的样式。

```csharp
Document doc = new Document();

// AddCopy 方法创建指定样式的副本，并且
// 自动为样式生成一个新名称，例如“Heading 1_0”。
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// 使用样式的“名称”属性来更改样式的识别名称。
newStyle.Name = "My Heading 1";

// 我们的文档现在有两种外观相同但名称不同的样式。
// 更改其中一种样式的设置不会影响另一种样式。
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### 也可以看看

* class [Style](../../style/)
* class [StyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
