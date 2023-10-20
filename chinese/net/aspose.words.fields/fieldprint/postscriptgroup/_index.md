---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: 用于 .NET 的 Aspose.Words
description: FieldPrint PostScriptGroup 财产. 获取或设置 PostScript 指令操作的绘图矩形 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

获取或设置 PostScript 指令操作的绘图矩形。

```csharp
public string PostScriptGroup { get; set; }
```

## 例子

显示插入 PRINT 字段。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// PRINT 字段可以向打印机发送指令。
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// 设置打印机执行指令的区域。
// 在本例中，它将是包含 PRINT 字段的段落。
field.PostScriptGroup = "para";

// 当我们使用支持PostScript的打印机来打印我们的文档时，
// 该命令会将我们在“field.PostScriptGroup”中指定的整个区域变成白色。
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### 也可以看看

* class [FieldPrint](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
