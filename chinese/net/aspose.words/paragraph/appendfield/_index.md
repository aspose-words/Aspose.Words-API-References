---
title: Paragraph.AppendField
linktitle: AppendField
articleTitle: AppendField
second_title: Aspose.Words for .NET
description: 使用 Paragraph AppendField 方法增强您的文档，无缝地将自定义字段添加到段落以改善组织性和清晰度。
type: docs
weight: 260
url: /zh/net/aspose.words/paragraph/appendfield/
---
## AppendField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#appendfield}

将字段附加到此段落。

```csharp
public Field AppendField(FieldType fieldType, bool updateField)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldType | FieldType | 要附加的字段的类型。 |
| updateField | Boolean | 指定是否立即更新字段。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)表示附加字段的对象。

## 例子

展示将字段附加到段落的各种方法。

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// 以下是将字段附加到段落末尾的三种方法。
// 1 - 使用字段类型附加 DATE 字段，然后更新它：
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - 使用字段代码附加 TIME 字段：
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - 使用字段代码附加 QUOTE 字段，并使其显示占位符值：
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// 此字段将显示其占位符值，直到我们更新它。
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## AppendField(*string*) {#appendfield_1}

将字段附加到此段落。

```csharp
public Field AppendField(string fieldCode)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | String | 要附加的字段代码（不带花括号）。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)表示附加字段的对象。

## 例子

展示将字段附加到段落的各种方法。

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// 以下是将字段附加到段落末尾的三种方法。
// 1 - 使用字段类型附加 DATE 字段，然后更新它：
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - 使用字段代码附加 TIME 字段：
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - 使用字段代码附加 QUOTE 字段，并使其显示占位符值：
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// 此字段将显示其占位符值，直到我们更新它。
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## AppendField(*string, string*) {#appendfield_2}

将字段附加到此段落。

```csharp
public Field AppendField(string fieldCode, string fieldValue)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldCode | String | 要附加的字段代码（不带花括号）。 |
| fieldValue | String | 要附加的字段值。传递`无效的`对于没有值的字段。 |

### 返回值

一个[`Field`](../../../aspose.words.fields/field/)表示附加字段的对象。

## 例子

展示将字段附加到段落的各种方法。

```csharp
Document doc = new Document();
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;

// 以下是将字段附加到段落末尾的三种方法。
// 1 - 使用字段类型附加 DATE 字段，然后更新它：
paragraph.AppendField(FieldType.FieldDate, true);

 // 2 - 使用字段代码附加 TIME 字段：
paragraph.AppendField(" TIME  \\@ \"HH:mm:ss\" ");

// 3 - 使用字段代码附加 QUOTE 字段，并使其显示占位符值：
paragraph.AppendField(" QUOTE \"Real value\"", "Placeholder value");

Assert.AreEqual("Placeholder value", doc.Range.Fields[2].Result);

// 此字段将显示其占位符值，直到我们更新它。
doc.UpdateFields();

Assert.AreEqual("Real value", doc.Range.Fields[2].Result);

doc.Save(ArtifactsDir + "Paragraph.AppendField.docx");
```

### 也可以看看

* class [Field](../../../aspose.words.fields/field/)
* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
