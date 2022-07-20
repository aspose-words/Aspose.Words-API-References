---
title: HorizontalPosition
second_title: Aspose.Words for .NET API 参考
description: 获取或设置字段后面的文本应从列框架或文本框的左边缘水平移动的点数 
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldadvance/horizontalposition/
---
## FieldAdvance.HorizontalPosition property

获取或设置字段后面的文本应从列、框架或文本框的左边缘水平移动的点数 。

```csharp
public string HorizontalPosition { get; set; }
```

### 例子

显示如何插入 ADVANCE 字段并编辑其属性。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// 下面是使用 ADVANCE 字段调整其后文本位置的两种方法。
// 继续应用 ADVANCE 字段的效果，直到段落结束，
// 或另一个 ADVANCE 字段更新偏移/坐标值。
// 1 - 指定方向偏移：
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - 将文本移动到坐标指定的位置：
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### 也可以看看

* class [FieldAdvance](../../fieldadvance)
* 命名空间 [Aspose.Words.Fields](../../fieldadvance)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->