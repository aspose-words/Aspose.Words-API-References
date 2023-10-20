---
title: FieldBarcode.IsBookmark
linktitle: IsBookmark
articleTitle: IsBookmark
second_title: Aspose.Words لـ .NET
description: FieldBarcode IsBookmark ملكية. يحصل على أو يحدد ما إذا كانPostalAddress هو اسم الإشارة المرجعية في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldbarcode/isbookmark/
---
## FieldBarcode.IsBookmark property

يحصل على أو يحدد ما إذا كان[`PostalAddress`](../postaladdress/) هو اسم الإشارة المرجعية.

```csharp
public bool IsBookmark { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقل BARCODE لعرض الرموز البريدية الأمريكية على شكل باركود.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln();

// فيما يلي طريقتان لاستخدام حقول الباركود لعرض القيم المخصصة كرموز شريطية.
// 1 - قم بتخزين القيمة التي سيعرضها الباركود في خاصية العنوان البريدي:
FieldBarcode field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);

// يجب أن تكون هذه القيمة رمزًا بريديًا صالحًا.
field.PostalAddress = "96801";
field.IsUSPostalAddress = true;
field.FacingIdentificationMark = "C";

Assert.AreEqual(" BARCODE  96801 \\u \\f C", field.GetFieldCode());

builder.InsertBreak(BreakType.LineBreak);

// 2 - إشارة مرجعية تخزن القيمة التي سيعرضها هذا الرمز الشريطي:
field = (FieldBarcode)builder.InsertField(FieldType.FieldBarcode, true);
field.PostalAddress = "BarcodeBookmark";
field.IsBookmark = true;

Assert.AreEqual(" BARCODE  BarcodeBookmark \\b", field.GetFieldCode());

// الإشارة المرجعية التي يشير إليها حقل BARCODE في خاصية PostalAddress الخاصة به
// يجب ألا يحتوي على أي شيء إلى جانب الرمز البريدي الصالح.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("BarcodeBookmark");
builder.Writeln("968877");
builder.EndBookmark("BarcodeBookmark");

doc.Save(ArtifactsDir + "Field.BARCODE.docx");
```

### أنظر أيضا

* class [FieldBarcode](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
