---
title: FieldShape Class
linktitle: FieldShape
articleTitle: FieldShape
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.FieldShape 类，轻松实现 SHAPE 字段。强大的功能和灵活性增强文档设计。
type: docs
weight: 2820
url: /zh/net/aspose.words.fields/fieldshape/
---
## FieldShape class

实现 SHAPE 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldShape : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldShape](fieldshape/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end/) { get; } | 获取代表字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format/) { get; } | 获得[`FieldFormat`](../fieldformat/)提供对字段格式进行类型化访问的对象。 |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | 获取或设置字段的当前结果是否由于对文档所做的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | 获取或设置字段的 LCID。 |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | 获取表示字段分隔符的节点。可以是`无效的`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | 获取表示字段开始的节点。 |
| [Text](../../aspose.words.fields/fieldshape/text/) { get; set; } | 获取或设置要检索的文本。 |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

检索指定的文本。

## 例子

展示如何使用 BIDIOUTLINE 字段创建从右到左的语言兼容列表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE 字段像 AUTONUM/LISTNUM 字段一样对段落进行编号，
// 但仅在启用从右到左的编辑语言（例如希伯来语或阿拉伯语）时才可见。
// 以下字段将显示“.1”，即列表编号“1.”的 RTL 等效项。
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// 再添加两个 BIDIOUTLINE 字段，分别显示“.2”和“.3”。
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

展示在加载过程中如何处理一些较旧的 Microsoft Word 字段（例如 SHAPE 和 EMBED）。

```csharp
// 打开在 Microsoft Word 2003 中创建的文档。
Document doc = new Document(MyDir + "Legacy fields.doc");

// 如果我们打开 Word 文档并按 Alt+F9，我们将看到一个 SHAPE 和一个 EMBED 字段。
// SHAPE 字段是启用了“嵌入文本”环绕样式的自选图形对象的锚点/画布。
// EMBED 字段具有相同的功能，但对于嵌入对象，
// 例如来自外部 Excel 文档的电子表格。
// 但是，这些字段不会出现在文档的字段集合中。
Assert.AreEqual(0, doc.Range.Fields.Count);

// 这些字段仅受旧版本的 Microsoft Word 支持。
// 文档加载过程会将这些字段转换为 Shape 对象，
// 我们可以在文档的节点集合中访问它。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// 第一个 Shape 节点对应于输入文档中的 SHAPE 字段，
// 这是自选图形的内联画布。
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// 第二个 Shape 节点是 AutoShape 本身。
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// 第三个形状是包含外部电子表格的 EMBED 字段。
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
