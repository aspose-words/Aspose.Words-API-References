---
title: FieldListNum Class
linktitle: FieldListNum
articleTitle: FieldListNum
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldListNum 班级. 实现 LISTNUM 字段 在 C#.
type: docs
weight: 2120
url: /zh/net/aspose.words.fields/fieldlistnum/
---
## FieldListNum class

实现 LISTNUM 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldListNum : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldListNum](fieldlistnum/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [HasListName](../../aspose.words.fields/fieldlistnum/haslistname/) { get; } | 返回一个值，该值指示抽象编号定义 的名称是否由字段代码提供。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [ListLevel](../../aspose.words.fields/fieldlistnum/listlevel/) { get; set; } | 获取或设置列表中的级别，覆盖字段的默认行为。 |
| [ListName](../../aspose.words.fields/fieldlistnum/listname/) { get; set; } | 获取或设置用于编号的抽象编号定义的名称。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| [StartingNumber](../../aspose.words.fields/fieldlistnum/startingnumber/) { get; set; } | 获取或设置此字段的起始值。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除该字段。返回字段后面的节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果该字段已被更新，则抛出异常。 |

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

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
