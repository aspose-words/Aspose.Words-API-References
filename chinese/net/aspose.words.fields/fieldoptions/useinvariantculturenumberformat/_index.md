---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words for .NET
description: 探索 FieldOptions UseInvariantCultureNumberFormat 属性，轻松管理具有不变文化的数字格式，以实现一致的数据处理。
type: docs
weight: 210
url: /zh/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

获取或设置指示使用不变文化解析数字格式的值或不

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## 评论

当此属性设置为`真的`，数字格式取自不变的文化。

当此属性设置为`错误的` ，数字格式取自当前线程的文化。

默认值为`错误的`。

## 例子

展示如何根据不变的文化来格式化数字。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // 有时，在某些文化下，字段可能无法正确格式化其数字。
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1.234.567,89 ,     ", field.Result);

// 为了解决这个问题，我们可以改变整个线程的文化。
// 解决这个问题的另一种方法是设置这个标志，
// 这使得所有字段在格式化数字时使用不变的文化。
// 这样我们就可以避免改变整个线程的文化。
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### 也可以看看

* class [FieldOptions](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
