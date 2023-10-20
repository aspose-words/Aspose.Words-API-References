---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder InsertField 方法. 将 Word 字段插入到文档中并可选择更新字段结果 在 C#.
type: docs
weight: 320
url: /zh/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

将 Word 字段插入到文档中，并可选择更新字段结果。

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | FieldType | 要附加的字段的类型。 |
| updateField | Boolean | 指定是否立即更新字段。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)表示插入字段的对象。

## 评论

此方法将字段插入到文档中。 Aspose.Words 可以更新大多数类型的字段，但不是全部。有关详细信息，请参阅 `InsertField`超载。

## 例子

演示如何使用 FieldType 将字段插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个字段，同时传递一个标志，该标志确定是否在构建器插入它们时更新它们。
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

    // 我们需要手动使用更新方法更新这些字段。
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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

将 Word 字段插入文档并更新字段结果。

```csharp
public Field InsertField(string fieldCode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | String | 要插入的域代码（不带花括号）。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)表示插入字段的对象。

## 评论

此方法将字段插入文档并立即更新字段结果。 Aspose.Words 可以更新大多数类型的字段，但不是全部。有关详细信息，请参阅 `InsertField`超载。

## 例子

演示如何使用域代码将域插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// InsertField 方法的这个重载会自动更新插入的字段。
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

显示如何插入字段，并将文档构建器的光标移动到它们。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// 将光标移动到第一个 MERGEFIELD。
builder.MoveToMergeField("MyMergeField1", true, false);

// 请注意，光标位于第一个 MERGEFIELD 之后，第二个之前。
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// 如果我们希望使用构建器编辑字段的字段代码或内容，
// 它的光标需要在一个字段内。
// 要将其放置在字段中，我们需要调用文档构建器的 MoveTo 方法
// 并将字段的开始或分隔节点作为参数传递。
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

将 Word 字段插入文档而不更新字段结果。

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | String | 要插入的域代码（不带花括号）。 |
| fieldValue | String | 要插入的字段值。为没有值的字段传递 null。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)表示插入字段的对象。

## 评论

Microsoft Word 文档中的字段由字段代码和字段结果组成。 字段代码就像一个公式，字段结果就像 公式产生的值。字段代码还可能包含字段switchs ，类似于执行特定操作的附加指令。

您可以使用键盘快捷键 Alt+F9 在文档 in Microsoft Word 中显示域代码和结果之间切换。字段代码出现在大括号 ( { } ) 之间。

要创建字段，您需要指定字段类型、字段代码和“占位符”字段值。 如果您不确定特定的字段代码语法，请先在 Microsoft Word 中创建字段 并切换以查看其字段代码.

Aspose.Words可以计算大部分字段类型的字段结果，但是这个方法 不会自动更新字段结果。因为字段结果不是自动计算的， 你应该传递一些字符串值（甚至是一个空字符串），这些值将被插入到字段结果中。 这个值将作为占位符保留在字段结果中，直到字段被updated. 要更新字段结果，您可以调用[`Update`](../../../aspose.words.fields/field/update/)在字段对象上返回 给您或[`UpdateFields`](../../document/updatefields/)更新整个文档中的字段。

## 例子

显示如何在部分中设置页码。

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

// 将文档构建器移动到第一部分的主标题，
// 该部分中的每个页面都将显示。
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// 插入一个 PAGE 字段，它将显示当前页的编号。
builder.Write("Page ");
builder.InsertField("PAGE", "");

// 配置部分以使 PAGE 字段显示的页数从 5 开始。
// 另外，将所有 PAGE 字段配置为使用大写罗马数字显示其页码。
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// 为第二个部分创建另一个主标题，带有另一个 PAGE 字段。
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// 将部分配置为使 PAGE 字段显示的页数从 10 开始。
// 另外，将所有 PAGE 字段配置为使用阿拉伯数字显示其页码。
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
