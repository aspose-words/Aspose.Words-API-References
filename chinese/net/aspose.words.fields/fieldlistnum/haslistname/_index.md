---
title: FieldListNum.HasListName
linktitle: HasListName
articleTitle: HasListName
second_title: 用于 .NET 的 Aspose.Words
description: FieldListNum HasListName 财产. 返回一个值该值指示抽象编号定义 的名称是否由字段代码提供 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldlistnum/haslistname/
---
## FieldListNum.HasListName property

返回一个值，该值指示抽象编号定义 的名称是否由字段代码提供。

```csharp
public bool HasListName { get; }
```

## 例子

演示如何使用 LISTNUM 字段对段落进行编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM 字段显示一个在每个 LISTNUM 字段处递增的数字。
// 这些字段还具有多种选项，允许我们使用它们来模拟编号列表。
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// 列表默认从 1 开始计数，但我们可以将此数字设置为不同的值，例如 0。
// 该字段将显示“0)”。
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

 // LISTNUM 字段为每个列表级别维护单独的计数。
// 在同一段落中插入一个 LISTNUM 字段作为另一个 LISTNUM 字段
// 增加列表级别而不是计数。
// 下一个字段将继续我们上面开始的计数，并在列表级别 1 处显示值“1”。
builder.InsertField(FieldType.FieldListNum, true);

// 该字段将从列表级别 2 开始计数。它将显示值“1”。
builder.InsertField(FieldType.FieldListNum, true);

// 该字段将从列表级别 3 开始计数。它将显示值“1”。
// 不同的列表级别有不同的格式，
// 因此这些字段组合后将显示值“1)a)i)”。
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// 我们插入的下一个 LISTNUM 字段将在列表级别继续计数
// 先前的 LISTNUM 字段已打开。
// 我们可以使用“ListLevel”属性跳转到不同的列表级别。
// 如果这个 LISTNUM 字段停留在列表级别 3，它将显示“ii)”，
// 但是，由于我们已将其移至列表级别 2，因此它会在该级别进行计数并显示“b)”。
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// 我们可以设置 ListName 属性来让字段模拟不同的 AUTONUM 字段类型。
// “NumberDefault”模拟 AUTONUM，“OutlineDefault”模拟 AUTONUMOUT，
// 和“LegalDefault”模拟 AUTONUMLGL 字段。
// 以 1 为起始编号的“OutlineDefault”列表名称将导致显示“I.”。
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName 不会从前一个字段继承，因此我们需要为每个新字段设置它。
// 该字段以不同的列表名称继续计数并显示“II.”。
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 5");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.LISTNUM.docx");
```

### 也可以看看

* class [FieldListNum](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
