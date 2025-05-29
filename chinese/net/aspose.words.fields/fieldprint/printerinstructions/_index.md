---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words for .NET
description: 了解如何使用 FieldPrint PrinterInstructions 管理打印机特定的控制代码和 PostScript 指令，以优化打印解决方案。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

获取或设置打印机特定的控制代码字符或 PostScript 指令。

```csharp
public string PrinterInstructions { get; set; }
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
// 在这种情况下，它将是包含我们的 PRINT 字段的段落。
field.PostScriptGroup = "para";

// 当我们使用支持 PostScript 的打印机打印文档时，
// 此命令将把我们在“field.PostScriptGroup”中指定的整个区域变成白色。
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### 也可以看看

* class [FieldPrint](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
