---
title: FieldBidiOutline Class
linktitle: FieldBidiOutline
articleTitle: FieldBidiOutline
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldBidiOutline 班级. 实现 BIDIOUTLINE 字段 在 C#.
type: docs
weight: 1650
url: /zh/net/aspose.words.fields/fieldbidioutline/
---
## FieldBidiOutline class

实现 BIDIOUTLINE 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldBidiOutline : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldBidiOutline](fieldbidioutline/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示的字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式的类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档进行的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结束之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
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

## 评论

此字段与 AUTONUMLGL 字段相同，但分隔段落编号的每个级别 的分隔符除外。

## 例子

演示如何使用 BIDIOUTLINE 字段创建从右到左的语言兼容列表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE 字段对段落进行编号，就像 AUTONUM/LISTNUM 字段一样，
// 但仅当启用从右到左编辑语言（例如希伯来语或阿拉伯语）时才可见。
// 以下字段将显示“.1”，RTL 相当于列表号“1.”。
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// 再添加两个 BIDIOUTLINE 字段，将显示“.2”和“.3”。
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// 将文档中每个段落的水平文本对齐方式设置为 RTL。
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// 如果我们在 Microsoft Word 中启用从右到左的编辑语言，我们的字段将显示数字。
// 否则，它们将显示“###”。
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
