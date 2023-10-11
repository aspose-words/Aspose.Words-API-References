---
title: Enum TextFormFieldType
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.TextFormFieldType 枚举. 指定文本表单字段的类型
type: docs
weight: 2770
url: /zh/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

指定文本表单字段的类型。

```csharp
public enum TextFormFieldType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Regular | `0` | 文本表单字段可以包含任何文本。 |
| Number | `1` | 文本表单字段只能包含数字。 |
| Date | `2` | 文本表单字段只能包含有效的日期值。 |
| CurrentDate | `3` | 文本表单字段值是字段更新时的当前日期。 |
| CurrentTime | `4` | 文本表单字段值是该字段更新的当前时间。 |
| Calculated | `5` | 文本表单字段值是根据 中指定的表达式计算的[`TextInputDefault`](../formfield/textinputdefault/)属性. |

### 例子

展示如何创建表单字段。

```csharp
DocumentBuilder builder = new DocumentBuilder();

// 表单字段是文档中的对象，用户可以通过提示输入值来与之交互。
// 我们可以使用文档生成器创建它们，下面是两种方法。
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

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


