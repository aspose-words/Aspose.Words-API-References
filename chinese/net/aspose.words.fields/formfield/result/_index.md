---
title: FormField.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words for .NET
description: 发现 FormField Result 属性，轻松管理和自定义表单字段的字符串输出，以增强用户体验。
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

对于复选框表单字段，结果可以是“1”或“0”来表示选中或未选中。

对于下拉表单字段，结果是下拉菜单中选择的字符串。

环境`Result`对于文本表单字段，不适用在[`TextInputFormat`](../textinputformat/)。如果要设置值并应用 格式，请使用[`SetTextInputValue`](../settextinputvalue/)方法。

对于文本表单字段[`TextInputDefault`](../textinputdefault/)如果应用了值 *value*是`无效的`。

## 例子

显示如何插入组合框。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// 插入一个组合框，允许用户从字符串集合中选择一个选项。
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// 表单字段将以“select”html标签的形式出现。
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### 也可以看看

* class [FormField](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
