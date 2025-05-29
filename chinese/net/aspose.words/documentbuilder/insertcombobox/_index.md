---
title: DocumentBuilder.InsertComboBox
linktitle: InsertComboBox
articleTitle: InsertComboBox
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 InsertComboBox 方法增强您的文档。轻松添加交互式组合框表单字段，提升用户体验。
type: docs
weight: 300
url: /zh/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

在当前位置插入组合框表单字段。

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 表单字段的名称。可以为空字符串。超过 20 个字符的值将被截断。 |
| items | String[] | 组合框的项目。最多 25 个项目。 |
| selectedIndex | Int32 | 组合框中选定项目的索引。 |

### 返回值

刚刚插入的表单字段节点。

## 评论

如果您为表单字段指定名称，则会自动创建具有相同名称的书签。

## 例子

展示如何将组合框表单字段插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个表单，提示用户从菜单中选择一项。
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

展示如何创建表单字段。

```csharp
DocumentBuilder builder = new DocumentBuilder();

// 表单字段是文档中的对象，用户可以通过提示输入值来与之交互。
// 我们可以使用文档构建器创建它们，下面是两种方法。
// 1 - 基本文本输入：
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 - 带有提示文本和一系列可能值的组合框：
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### 也可以看看

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
