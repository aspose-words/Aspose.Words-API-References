---
title: DocumentBuilder.InsertCheckBox
linktitle: InsertCheckBox
articleTitle: InsertCheckBox
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder InsertCheckBox 方法. 在当前位置插入复选框表单字段 在 C#.
type: docs
weight: 290
url: /zh/net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(*string, bool, int*) {#insertcheckbox_1}

在当前位置插入复选框表单字段。

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 表单字段的名称。可以是空字符串。超过 20 个字符的值将被截断。 |
| checkedValue | Boolean | 已检查复选框表单字段的状态。 |
| size | Int32 | 指定复选框的大小（以磅为单位）。为 MS Word 指定 0 以自动计算复选框的大小。 |

### 返回值

刚刚插入的表单字段节点。

## 评论

如果您为表单字段指定名称，则会自动创建同名的书签。

## 例子

演示如何将复选框插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入不同大小和默认选中状态的复选框。
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// 表单字段的名称长度限制为 20 个字符。
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// 我们可以通过双击 Microsoft Word 中的这些复选框进行交互。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### 也可以看看

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertCheckBox(*string, bool, bool, int*) {#insertcheckbox}

在当前位置插入复选框表单字段。

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 表单字段的名称。可以是空字符串。超过 20 个字符的值将被截断。 |
| defaultValue | Boolean | 复选框表单字段的默认值。 |
| checkedValue | Boolean | 复选框表单字段的当前选中状态。 |
| size | Int32 | 指定复选框的大小（以磅为单位）。为 MS Word 指定 0 以自动计算复选框的大小。 |

### 返回值

刚刚插入的表单字段节点。

## 评论

如果您为表单字段指定名称，则会自动创建同名的书签。

## 例子

演示如何将复选框插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入不同大小和默认选中状态的复选框。
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// 表单字段的名称长度限制为 20 个字符。
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// 我们可以通过双击 Microsoft Word 中的这些复选框进行交互。
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### 也可以看看

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
