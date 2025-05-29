---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words for .NET
description: 探索 FieldOptions LegacyNumberFormat 属性以启用或禁用字段的旧式数字格式，增强兼容性和性能。
type: docs
weight: 160
url: /zh/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

获取或设置指示是否启用字段的旧式（早于 AW 13.10）数字格式的值。

```csharp
public bool LegacyNumberFormat { get; set; }
```

## 评论

当此属性设置为`真的`，模板符号“#”的作用类似于 .net: ，如果存在井号，则用相应的数字替换井号；否则，结果字符串中不会出现任何符号。

当此属性设置为`错误的`模板符号“#”的作用类似于 MS Word: 。此格式项指定结果中必须显示的数字位数。 如果结果中该位数没有数字，MS Word 将显示一个空格。例如，{ = 9 + 6 \# $### } 显示 $ 15。

默认值为`错误的`。

## 例子

显示如何为字段启用旧式数字格式。

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
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
