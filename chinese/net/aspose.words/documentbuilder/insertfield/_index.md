---
title: DocumentBuilder.InsertField
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将 Word 字段插入文档并可选择更新字段结果
type: docs
weight: 330
url: /zh/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(FieldType, bool) {#insertfield}

将 Word 字段插入文档并可选择更新字段结果。

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | FieldType | 要附加的字段的类型。 |
| updateField | Boolean | 指定是否立即更新该字段。 |

### 返回值

A[`Field`](../../../aspose.words.fields/field/)代表插入字段的对象。

### 评论

此方法将字段插入到文档中。 Aspose.Words 可以更新大多数类型的字段，但不是全部。欲了解更多详情，请参阅 `InsertField`超载。

### 例子

演示如何使用 FieldType 将字段插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个字段，同时传递一个标志，该标志确定在构建器插入它们时是否更新它们。
// 在某些情况下，更新字段的计算成本可能很高，推迟更新可能是个好主意。
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // 我们需要使用更新方法手动更新这些字段。
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertField(string) {#insertfield_1}

将 Word 字段插入文档并更新字段结果。

```csharp
public Field InsertField(string fieldCode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | String | 要插入的字段代码（不带花括号）。 |

### 返回值

A[`Field`](../../../aspose.words.fields/field/)代表插入字段的对象。

### 评论

此方法将字段插入到文档中并立即更新字段结果。 Aspose.Words 可以更新大多数类型的字段，但不是全部。欲了解更多详情，请参阅 `InsertField`超载。

### 例子

演示如何使用域代码将域插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField 方法的此重载会自动更新插入的字段。
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

演示如何插入字段，以及如何将文档生成器的光标移至这些字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// 将光标移动到第一个 MERGEFIELD。
builder.MoveToMergeField("MyMergeField1", true, false);

// 请注意，光标紧邻第一个 MERGEFIELD 之后和第二个 MERGEFIELD 之前。
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// 如果我们希望使用构建器编辑字段的字段代码或内容，
// 它的光标需要位于字段内。
// 要将其放置在字段中，我们需要调用文档构建器的 MoveTo 方法
// 并将字段的开始或分隔符节点作为参数传递。
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)

---

## InsertField(string, string) {#insertfield_2}

将 Word 字段插入到文档中，而不更新字段结果。

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | String | 要插入的字段代码（不带花括号）。 |
| fieldValue | String | 要插入的字段值。经过`无效的`对于没有值的字段。 |

### 返回值

A[`Field`](../../../aspose.words.fields/field/)代表插入字段的对象。

### 评论

Microsoft Word 文档中的字段由字段代码和字段结果组成。 字段代码就像一个公式，字段结果就像 公式生成的值。字段代码还可以包含字段switches ，类似于执行特定操作的附加指令。

您可以使用键盘快捷键 Alt+F9 在 in Microsoft Word 文档中的显示域代码和结果之间进行切换。字段代码出现在大括号 ( { } ) 之间。

要创建字段，您需要指定字段类型、字段代码和“占位符”字段值。 如果您不确定特定字段代码语法，请先在 Microsoft Word 中创建字段 并切换以查看其字段代码。

Aspose.Words可以计算大多数字段类型的字段结果，但此方法 不会自动更新字段结果。由于字段结果不会自动计算， 您需要传递一些将插入到字段结果中的字符串值（甚至是空字符串）。 该值将作为占位符保留在字段结果中，直到字段被Updated. 要更新字段结果，您可以调用[`Update`](../../../aspose.words.fields/field/update/)在字段对象 returned 上或[`UpdateFields`](../../document/updatefields/)更新整个文档中的字段。

### 例子

展示如何在节中设置页码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// 将文档生成器移动到第一部分的主标题，
// 该部分中的每个页面都会显示。
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// 插入一个PAGE字段，该字段将显示当前页码。
builder.Write("Page ");
builder.InsertField("PAGE", "");

// 配置该部分，使 PAGE 字段显示的页数从 5 开始。
// 另外，配置所有 PAGE 字段以使用大写罗马数字显示其页码。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// 使用另一个 PAGE 字段为第二部分创建另一个主标头。
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// 配置该部分，使 PAGE 字段显示的页数从 10 开始。
// 另外，配置所有 PAGE 字段以使用阿拉伯数字显示其页码。
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


