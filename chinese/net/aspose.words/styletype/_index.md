---
title: StyleType Enum
linktitle: StyleType
articleTitle: StyleType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.StyleType 枚举，高效管理文档中的样式。使用多种样式类型增强您的格式，获得最佳效果！
type: docs
weight: 7010
url: /zh/net/aspose.words/styletype/
---
## StyleType enumeration

表示样式的类型。

```csharp
public enum StyleType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Paragraph | `1` | 该样式为段落样式。 |
| Character | `2` | 该样式是一种字符样式。 |
| Table | `3` | 该样式是表格样式。 |
| List | `4` | 样式为列表样式。 |

## 例子

展示如何创建列表样式并在文档中使用它。

```csharp
Document doc = new Document();

// 列表允许我们使用前缀符号和缩进来组织和装饰段落集。
 // 我们可以通过增加缩进级别来创建嵌套列表。
 // 我们可以使用文档构建器的“ListFormat”属性来开始和结束列表。
// 我们在列表的开始和结束之间添加的每个段落都将成为列表中的一个项目。
// 我们可以在一种样式中包含整个列表对象。
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// 更改列表中所有列表级别的外观。
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// 从样式内的列表创建另一个列表。
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// 添加一些我们的列表将格式化的列表项。
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// 根据列表样式创建并应用另一个列表。
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
