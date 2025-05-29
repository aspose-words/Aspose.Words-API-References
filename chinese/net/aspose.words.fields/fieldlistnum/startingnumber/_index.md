---
title: FieldListNum.StartingNumber
linktitle: StartingNumber
articleTitle: StartingNumber
second_title: Aspose.Words for .NET
description: 探索 FieldListNum StartingNumber 属性，轻松管理字段的起始值，从而改善数据组织和效率。
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fieldlistnum/startingnumber/
---
## FieldListNum.StartingNumber property

获取或设置此字段的起始值。

```csharp
public string StartingNumber { get; set; }
```

## 例子

展示如何使用 LISTNUM 字段对段落进行编号。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// LISTNUM 字段显示一个在每个 LISTNUM 字段处递增的数字。
// 这些字段还具有多种选项，允许我们使用它们来模拟编号列表。
FieldListNum field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);

// 列表默认从 1 开始计数，但我们可以将此数字设置为不同的值，例如 0。
// 此字段将显示“0)”。
field.StartingNumber = "0";
builder.Writeln("Paragraph 1");

Assert.AreEqual(" LISTNUM  \\s 0", field.GetFieldCode());

// LISTNUM 字段为每个列表级别维护单独的计数。
// 将一个 LISTNUM 字段插入到与另一个 LISTNUM 字段相同的段落中
// 增加列表级别而不是计数。
// 下一个字段将继续我们上面开始的计数，并在列表级别 1 显示值“1”。
builder.InsertField(FieldType.FieldListNum, true);

// 此字段将从列表级别 2 开始计数。它将显示值“1”。
builder.InsertField(FieldType.FieldListNum, true);

// 此字段将从列表级别 3 开始计数。它将显示值“1”。
// 不同列表级别具有不同的格式，
// 因此这些字段组合起来将显示值“1)a)i)”。
builder.InsertField(FieldType.FieldListNum, true);
builder.Writeln("Paragraph 2");

// 我们插入的下一个 LISTNUM 字段将继续列表级别的计数
// 先前的 LISTNUM 字段处于打开状态。
// 我们可以使用“ListLevel”属性跳转到不同的列表级别。
// 如果此 LISTNUM 字段停留在列表级别 3，它将显示“ii)”，
// 但是，由于我们已将其移动到列表级别 2，它会继续在该级别计数并显示“b)”。
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.ListLevel = "2";
builder.Writeln("Paragraph 3");

Assert.AreEqual(" LISTNUM  \\l 2", field.GetFieldCode());

// 我们可以设置 ListName 属性来让字段模拟不同的 AUTONUM 字段类型。
// “NumberDefault” 模拟 AUTONUM，“OutlineDefault” 模拟 AUTONUMOUT，
// 并且“LegalDefault”模拟 AUTONUMLGL 字段。
// 以 1 作为起始数字的“OutlineDefault”列表名称将显示“I。”。
field = (FieldListNum)builder.InsertField(FieldType.FieldListNum, true);
field.StartingNumber = "1";
field.ListName = "OutlineDefault";
builder.Writeln("Paragraph 4");

Assert.IsTrue(field.HasListName);
Assert.AreEqual(" LISTNUM  OutlineDefault \\s 1", field.GetFieldCode());

// ListName 不会从前一个字段继承，因此我们需要为每个新字段设置它。
// 该字段继续以不同的列表名称进行计数，并显示“II。”。
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
