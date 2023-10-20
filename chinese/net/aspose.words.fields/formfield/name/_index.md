---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: 用于 .NET 的 Aspose.Words
description: FormField Name 财产. 获取或设置表单字段名称 在 C#.
type: docs
weight: 130
url: /zh/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

获取或设置表单字段名称。

```csharp
public string Name { get; set; }
```

## 评论

Microsoft Word 允许最多包含 20 个字符的字符串。

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

// 表单域将以“select”html标签的形式出现。
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### 也可以看看

* class [FormField](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
