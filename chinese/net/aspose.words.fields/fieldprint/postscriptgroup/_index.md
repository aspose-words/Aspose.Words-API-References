---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words for .NET
description: 发现 FieldPrint PostScriptGroup 属性可以轻松管理绘图矩形，以实现高效的 PostScript 指令处理。
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
