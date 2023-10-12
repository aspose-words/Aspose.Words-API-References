---
title: Class FieldEmbed
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.FieldEmbed 班级. 实现 EMBED 字段
type: docs
weight: 1850
url: /zh/net/aspose.words.fields/fieldembed/
---
## FieldEmbed class

实现 EMBED 字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class FieldEmbed : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldEmbed](fieldembed/)() | 默认构造函数。 |

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
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中删除该字段。返回字段后面的节点。如果字段的结尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被删除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/)() | 执行字段更新。如果该字段已被更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/)(bool) | 执行字段更新。如果该字段已被更新，则抛出异常。 |

### 例子

显示加载过程中如何处理一些较旧的 Microsoft Word 字段（例如 SHAPE 和 EMBED）。

```csharp
// 打开在 Microsoft Word 2003 中创建的文档。
Document doc = new Document(MyDir + "Legacy fields.doc");

// 如果我们打开 Word 文档并按 Alt+F9，我们将看到一个 SHAPE 和一个 EMBED 字段。
// SHAPE 字段是启用了“与文本对齐”环绕样式的自选图形对象的锚点/画布。
// EMBED 字段具有相同的功能，但对于嵌入对象来说，
// 例如来自外部 Excel 文档的电子表格。
// 但是，这些字段不会出现在文档的 Fields 集合中。
Assert.AreEqual(0, doc.Range.Fields.Count);

// 这些字段仅受旧版本的 Microsoft Word 支持。
// 文档加载过程会将这些字段转换为Shape对象，
// 我们可以在文档的节点集合中访问它。
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);
Assert.AreEqual(3, shapes.Count);

// 第一个 Shape 节点对应于输入文档中的 SHAPE 字段，
// 这是自选图形的内联画布。
Shape shape = (Shape)shapes[0];
Assert.AreEqual(ShapeType.Image, shape.ShapeType);

// 第二个 Shape 节点是自选图形本身。
shape = (Shape)shapes[1];
Assert.AreEqual(ShapeType.Can, shape.ShapeType);

// 第三个 Shape 是包含外部电子表格的 EMBED 字段。
shape = (Shape)shapes[2];
Assert.AreEqual(ShapeType.OleObject, shape.ShapeType);
```

### 也可以看看

* class [Field](../field/)
* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


