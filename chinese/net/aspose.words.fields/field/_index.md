---
title: Field Class
linktitle: Field
articleTitle: Field
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.Field 类，这是使用动态字段增强 Microsoft Word 文档以提高功能和效率的关键。
type: docs
weight: 1920
url: /zh/net/aspose.words.fields/field/
---
## Field class

表示 Microsoft Word 文档字段。

要了解更多信息，请访问[使用字段](https://docs.aspose.com/words/net/working-with-fields/)文档文章。

```csharp
public class Field
```

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
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | 获取 Microsoft Word 字段类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包括子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/#getfieldcode_1)(*bool*) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove/)() | 从文档中移除该字段。返回紧接该字段之后的节点。如果该字段的末尾是其父节点的最后一个 child ，则返回其父段落。如果该字段已被移除，则返回`无效的`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update/#update)() | 执行字段更新。如果字段已在更新，则抛出异常。 |
| [Update](../../aspose.words.fields/field/update/#update_1)(*bool*) | 执行字段更新。如果字段已在更新，则抛出异常。 |

## 评论

Word 文档中的字段是一个复杂的结构，由多个节点组成，包括字段起始、字段代码、字段分隔符、字段结果和字段结束。字段可以嵌套，包含丰富的内容，并且可以在文档中跨多个段落或章节。字段`Field`类是一个“外观”对象，它提供 属性和方法，允许将字段作为单个对象来使用。

这[`Start`](./start/)，[`Separator`](./separator/)和[`End`](./end/)属性分别指向 字段的开始、分隔符和结束节点。

字段起始和分隔符之间的内容为字段代码， 字段分隔符和字段结束之间的内容为字段结果，字段代码通常由一个或多个 组成[`Run`](../../aspose.words/run/)指定指令的对象。处理应用程序需要执行 字段代码来计算字段结果。

计算字段结果的过程称为字段更新。Aspose.Words 可以更新大多数字段类型的 field 结果，其方式与 Microsoft Word 完全相同。最值得注意的是，Aspose.Words 甚至可以计算最复杂公式字段的结果。要计算单个字段的 field 结果，请使用[`Update`](./update/)方法。要更新整个 document 中的字段，请使用[`UpdateFields`](../../aspose.words/document/updatefields/)。

您可以使用以下方式获取字段代码的纯文本版本[`GetFieldCode`](./getfieldcode/)方法。 您可以使用获取和设置字段结果的纯文本版本[`Result`](./result/)属性。 字段代码和字段结果都可以包含复杂的内容，例如嵌套字段、段落、形状、 表，在这种情况下，如果您需要更多控制，您可能希望直接使用字段节点。

您无需创建`Field`直接使用类。 要创建新字段，请使用[`InsertField`](../../aspose.words/documentbuilder/insertfield/)方法。

## 例子

展示如何使用字段代码将字段插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField 方法的此重载会自动更新插入的字段。
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
