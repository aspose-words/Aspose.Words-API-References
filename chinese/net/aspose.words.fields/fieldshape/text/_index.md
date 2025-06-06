---
title: FieldShape.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words for .NET
description: 轻松管理 FieldShape 文本 - 轻松获取或设置值，以实现无缝数据检索和增强应用程序的功能。
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldshape/text/
---
## FieldShape.Text property

获取或设置要检索的文本。

```csharp
public string Text { get; set; }
```

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

* class [FieldShape](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
