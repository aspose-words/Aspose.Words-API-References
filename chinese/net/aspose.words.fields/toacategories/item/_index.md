---
title: ToaCategories.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 轻松管理您的 ToaCategories 项目。轻松按编号设置和检索类别标题，简化组织流程，提高效率。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/toacategories/item/
---
## ToaCategories indexer

通过类别编号获取或设置类别标题。

```csharp
public string this[int number] { get; set; }
```

## 例子

展示如何为 TOA 字段指定一组类别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOA 字段可以按照此集合中定义的类别过滤其条目。
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// 此类别集合带有默认值，我们可以用自定义值覆盖它。
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// 我们始终可以通过此集合访问默认值。
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// 插入 2 个 TOA 字段。TOA 字段为文档中的每个 TA 字段创建一个条目。
// 使用“\c”开关从我们的集合中选择一个类别的索引。
// 使用此开关，TOA 字段将仅从 TA 字段中选取条目
// 也有一个带有匹配类别索引的“\c”开关。每个 TOA 字段还将显示
// 其“\c”开关指向的类别的名称。
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// 在两个类别中插入 TOA 条目。第一个 TOA 字段将接收一个条目，
// 来自第二个 TA 字段，其“\c”开关也指向第一个类别。
// 第二个 TOA 字段将包含来自其他两个 TA 字段的两个条目。
builder.InsertField("TA \\c 2 \\l \"entry 1\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 1 \\l \"entry 2\"");
builder.InsertBreak(BreakType.PageBreak);
builder.InsertField("TA \\c 2 \\l \"entry 3\"");

doc.UpdateFields();
doc.Save(ArtifactsDir + "FieldOptions.TOA.Categories.docx");
```

### 也可以看看

* class [ToaCategories](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
