---
title: FieldBarcode.PostalAddress
linktitle: PostalAddress
articleTitle: PostalAddress
second_title: 用于 .NET 的 Aspose.Words
description: FieldBarcode PostalAddress 财产. 获取或设置用于生成条形码的邮政地址或引用它的书签的名称 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.fields/fieldbarcode/postaladdress/
---
## FieldBarcode.PostalAddress property

获取或设置用于生成条形码的邮政地址或引用它的书签的名称。

```csharp
public string PostalAddress { get; set; }
```

## 例子

演示如何使用“条形码”字段以条形码的形式显示美国邮政编码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// 以下是使用条形码字段将自定义值显示为条形码的两种方法。
// 1 - 将条形码将显示的值存储在 PostalAddress 属性中：
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// 该值必须是有效的邮政编码。
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - 引用存储此条形码将显示的值的书签：
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// BARCODE 字段在其 PostalAddress 属性中引用的书签
// 除了有效的邮政编码之外不需要包含任何内容。
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### 也可以看看

* class [FieldBarcode](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
