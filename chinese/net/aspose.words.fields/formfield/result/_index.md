---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: 用于 .NET 的 Aspose.Words
description: FormField Result 财产. 获取或设置表示此表单字段结果的字符串 在 C#.
type: docs
weight: 170
url: /zh/net/aspose.words.fields/formfield/result/
---
## FormField.Result property

获取或设置表示此表单字段结果的字符串。

```csharp
public string Result { get; set; }
```

## 评论

对于文本表单字段，结果是字段中的文本。

对于复选框表单字段，结果可以是“1”或“0”来指示选中或未选中。

对于下拉表单字段，结果是在下拉列表中选择的字符串。

环境`Result`对于文本表单字段不应用中指定的文本格式 [`TextInputFormat`](../textinputformat/) 。如果您想设置一个值并应用 格式，请使用[`SetTextInputValue`](../settextinputvalue/)方法。

对于文本表单字段[`TextInputDefault`](../textinputdefault/)值已应用 如果*value*是`无效的`。

## 例子

演示如何插入组合框。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// 插入一个组合框，允许用户从字符串集合中选择一个选项。
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// 表单字段将以“select”html 标签的形式出现。
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### 也可以看看

* class [FormField](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
