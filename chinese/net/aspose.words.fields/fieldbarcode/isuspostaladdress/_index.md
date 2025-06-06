---
title: FieldBarcode.IsUSPostalAddress
linktitle: IsUSPostalAddress
articleTitle: IsUSPostalAddress
second_title: Aspose.Words for .NET
description: 探索 FieldBarcode 的 IsUSPostalAddress 属性。轻松管理美国邮政地址验证，实现精准数据处理并提高效率。
type: docs
weight: 40
url: /zh/net/aspose.words.fields/fieldbarcode/isuspostaladdress/
---
## FieldBarcode.IsUSPostalAddress property

获取或设置是否[`PostalAddress`](../postaladdress/)是美国邮政地址。

```csharp
public bool IsUSPostalAddress { get; set; }
```

## 例子

展示如何使用 BARCODE 字段以条形码的形式显示美国邮政编码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// 以下是两种使用 BARCODE 字段将自定义值显示为条形码的方法。
// 1 - 将条形码将显示的值存储在 PostalAddress 属性中：
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// 此值需要是有效的邮政编码。
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
// 除了有效的邮政编码外，不需要包含任何内容。
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
