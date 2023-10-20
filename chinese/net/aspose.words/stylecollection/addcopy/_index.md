---
title: StyleCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: 用于 .NET 的 Aspose.Words
description: StyleCollection AddCopy 方法. 将样式复制到此集合中 在 C#.
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

复制样式准备好使用。

## 评论

要复制的样式可以属于同一个文档，也可以属于不同的文档。

链接样式被复制。

此方法不会复制基本样式。

如果集合中已经包含同名样式，则新名称为 通过从0开始添加“_number”后缀自动生成，例如“Normal_0”、“Heading 1_1”等。 使用[`Name`](../../style/name/)setter 用于更改导入样式的名称。

## 例子

演示如何将样式从一个文档导入到另一个文档。

```csharp
Document srcDoc = new Document();

// 为源文档创建自定义样式。
Style srcStyle = srcDoc.Styles.Add(StyleType.Paragraph, "MyStyle");
srcStyle.Font.Color = Color.Red;

// 将源文档的自定义样式导入目标文档。
Document dstDoc = new Document();
Style newStyle = dstDoc.Styles.AddCopy(srcStyle);

// 导入的样式具有与其源样式相同的外观。
Assert.AreEqual("MyStyle", newStyle.Name);
Assert.AreEqual(Color.Red.ToArgb(), newStyle.Font.Color.ToArgb());
```

显示如何克隆文档的样式。

```csharp
Document doc = new Document();

// AddCopy 方法创建指定样式的副本并
// 自动为样式生成一个新名称，例如“Heading 1_0”。
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

// 使用样式的“名称”属性来更改样式的标识名称。
newStyle.Name = "My Heading 1";

// 我们的文档现在有两个外观相同但名称不同的样式。
// 更改其中一种样式的设置不会影响另一种。
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
