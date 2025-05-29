---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 InsertTextInput 方法轻松添加文本表单字段。立即提升文档的交互性和用户体验！
type: docs
weight: 510
url: /zh/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

在当前位置插入文本表单字段。

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| name | String | 表单字段的名称。可以为空字符串。 |
| type | TextFormFieldType | 指定文本表单字段的类型。 |
| format | String | 用于格式化表单字段值的格式字符串。 |
| fieldValue | String | 将显示在字段中的文本。 |
| maxLength | Int32 | 用户可在表单字段中输入的最大长度。设置为零表示长度不受限制。 |

### 返回值

刚刚插入的表单字段节点。

## 评论

如果您为表单字段指定名称，则会自动创建具有相同名称的书签。

## 例子

展示如何将文本输入表单字段插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入提示用户输入文本的表单。
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

展示如何插入文本输入表单字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// 插入一个文本输入字段，用户可以单击它并输入文本。
// 分配一些用户可以覆盖并传递的占位符文本
// 最大文本长度为 0，对表单字段的内容不施加限制。
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// 表单字段将以“input”html 标签的形式出现，类型为“text”。
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
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
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
