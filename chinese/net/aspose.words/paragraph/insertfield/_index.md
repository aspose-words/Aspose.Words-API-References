---
title: Paragraph.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words for .NET
description: 使用段落插入字段方法，轻松将字段插入段落。增强文档功能并简化内容管理。
type: docs
weight: 290
url: /zh/net/aspose.words/paragraph/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool, [Node](../../node/), bool*) {#insertfield}

在此段落中插入一个字段。

```csharp
public Field InsertField(FieldType fieldType, bool updateField, Node refNode, bool isAfter)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | FieldType | 要插入的字段的类型。 |
| updateField | Boolean | 指定是否立即更新字段。 |
| refNode | Node | 本段落内的参考节点（如果*refNode*是`无效的`，然后附加到段落末尾）。 |
| isAfter | Boolean | 是否将字段插入到参考节点之后或之前。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)代表插入字段的对象。

## 例子

展示向段落添加字段的各种方法。

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// 以下是将字段插入段落的三种方法。
// 1 - 在段落的某个子节点之后插入 AUTHOR 字段：
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - 在段落的某个子节点后插入一个 QUOTE 字段：
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - 在段落的某个子节点前插入一个 QUOTE 字段，
// 并让它显示一个占位符值：
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// 此字段将显示其占位符值，直到我们更新它。
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Node](../../node/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertField(*string, [Node](../../node/), bool*) {#insertfield_1}

在此段落中插入一个字段。

```csharp
public Field InsertField(string fieldCode, Node refNode, bool isAfter)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | String | 要插入的字段代码（不带花括号）。 |
| refNode | Node | 本段落内的参考节点（如果*refNode*是`无效的`，然后附加到段落末尾）。 |
| isAfter | Boolean | 是否将字段插入到参考节点之后或之前。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)代表插入字段的对象。

## 例子

展示向段落添加字段的各种方法。

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// 以下是将字段插入段落的三种方法。
// 1 - 在段落的某个子节点之后插入 AUTHOR 字段：
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - 在段落的某个子节点后插入一个 QUOTE 字段：
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - 在段落的某个子节点前插入一个 QUOTE 字段，
// 并让它显示一个占位符值：
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// 此字段将显示其占位符值，直到我们更新它。
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertField(*string, string, [Node](../../node/), bool*) {#insertfield_2}

在此段落中插入一个字段。

```csharp
public Field InsertField(string fieldCode, string fieldValue, Node refNode, bool isAfter)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | String | 要插入的字段代码（不带花括号）。 |
| fieldValue | String | 要插入的字段值。传递`无效的`对于没有值的字段。 |
| refNode | Node | 本段落内的参考节点（如果*refNode*是`无效的`，然后附加到段落末尾）。 |
| isAfter | Boolean | 是否将字段插入到参考节点之后或之前。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)代表插入字段的对象。

## 例子

展示向段落添加字段的各种方法。

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// 以下是将字段插入段落的三种方法。
// 1 - 在段落的某个子节点之后插入 AUTHOR 字段：
Run run = new Run(doc) { Text = "This run was written by " };
para.AppendChild(run);

doc.BuiltInDocumentProperties["Author"].Value = "John Doe";
para.InsertField(FieldType.FieldAuthor, true, run, true);

// 2 - 在段落的某个子节点后插入一个 QUOTE 字段：
run = new Run(doc) { Text = "." };
para.AppendChild(run);

Field field = para.InsertField(" QUOTE \" Real value\" ", run, true);

// 3 - 在段落的某个子节点前插入一个 QUOTE 字段，
// 并让它显示一个占位符值：
para.InsertField(" QUOTE \" Real value.\"", " Placeholder value.", field.Start, false);

Assert.AreEqual(" Placeholder value.", doc.Range.Fields[1].Result);

// 此字段将显示其占位符值，直到我们更新它。
doc.UpdateFields();

Assert.AreEqual(" Real value.", doc.Range.Fields[1].Result);

doc.Save(ArtifactsDir + "Paragraph.InsertField.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [Node](../../node/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
