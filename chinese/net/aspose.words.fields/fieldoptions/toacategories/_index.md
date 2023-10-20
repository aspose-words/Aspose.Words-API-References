---
title: FieldOptions.ToaCategories
linktitle: ToaCategories
articleTitle: ToaCategories
second_title: 用于 .NET 的 Aspose.Words
description: FieldOptions ToaCategories 财产. 获取或设置权限类别表 在 C#.
type: docs
weight: 200
url: /zh/net/aspose.words.fields/fieldoptions/toacategories/
---
## FieldOptions.ToaCategories property

获取或设置权限类别表。

```csharp
public ToaCategories ToaCategories { get; set; }
```

## 例子

演示如何为 TOA 字段指定一组类别。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// TOA 字段可以按此集合中定义的类别过滤其条目。
ToaCategories toaCategories = new ToaCategories();
doc.FieldOptions.ToaCategories = toaCategories;

// 这个类别集合带有默认值，我们可以用自定义值覆盖它。
Assert.AreEqual("Cases", toaCategories[1]);
Assert.AreEqual("Statutes", toaCategories[2]);

toaCategories[1] = "My Category 1";
toaCategories[2] = "My Category 2";

// 我们总是可以通过这个集合访问默认值。
Assert.AreEqual("Cases", ToaCategories.DefaultCategories[1]);
Assert.AreEqual("Statutes", ToaCategories.DefaultCategories[2]);

// 插入 2 个 TOA 字段。 TOA 字段为文档中的每个 TA 字段创建一个条目。
// 使用“\c”开关从我们的集合中选择类别的索引。
// 使用此开关，TOA 字段将仅从 TA 字段中选取条目
// 还有一个带有匹配类别索引的“\c”开关。每个 TOA 字段还将显示
// 其“\c”开关指向的类别的名称。
builder.InsertField("TOA \\c 1 \\h", null);
builder.InsertField("TOA \\c 2 \\h", null);
builder.InsertBreak(BreakType.PageBreak);

// 跨 2 个类别插入 TOA 条目。我们的第一个 TOA 字段将收到一个条目，
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

* class [ToaCategories](../../toacategories/)
* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
