---
title: FieldOptions.LegacyNumberFormat
second_title: Aspose.Words for .NET API 参考
description: FieldOptions 财产. 获取或设置指示是否启用字段的旧版早于 AW 13.10数字格式的值
type: docs
weight: 160
url: /zh/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

获取或设置指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。

```csharp
public bool LegacyNumberFormat { get; set; }
```

### 评论

当该属性设置为`真的`，模板符号“#”的工作方式与 .net: 中的井号符号替换为相应的数字（如果存在）；否则，结果字符串中不会出现任何符号。

当该属性设置为`错误的`，模板符号“#”用作 MS Word： 此格式项指定结果中显示的必需数字位置。 如果结果中不包含该位置的数字，MS Word 将显示一个空格。例如，{ = 9 + 6 \# $### } 显示 $ 15。

默认值为`错误的`。

### 例子

显示如何启用字段的旧数字格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../fieldoptions/)
* 部件 [Aspose.Words](../../../)


