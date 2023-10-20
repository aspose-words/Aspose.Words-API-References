---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: 用于 .NET 的 Aspose.Words
description: FieldOptions UseInvariantCultureNumberFormat 财产. 获取或设置指示使用不变区域性解析数字格式的值或 not 在 C#.
type: docs
weight: 210
url: /zh/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

获取或设置指示使用不变区域性解析数字格式的值或 not

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## 评论

当此属性设置为`真的`，数字格式取自不变区域性。

当此属性设置为`错误的` ，数字格式取自当前线程的区域性。

默认值为`错误的`。

## 例子

演示如何根据不变区域性设置数字格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // 有时，在某些文化下，字段可能无法正确格式化其数字。
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1234567,89 .     ", field.Result);

// 为了解决这个问题，我们可以更改整个线程的区域性。
// 解决此问题的另一种方法是设置此标志，
// 使所有字段在格式化数字时使用不变区域性。
// 这种方式允许我们避免更改整个线程的区域性。
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
