---
title: FieldBarcode.FacingIdentificationMark
linktitle: FacingIdentificationMark
articleTitle: FacingIdentificationMark
second_title: Aspose.Words لـ .NET
description: FieldBarcode FacingIdentificationMark ملكية. الحصول على أو تعيين نوع علامة التعريف المواجهة FIM المراد إدراجها في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldbarcode/facingidentificationmark/
---
## FieldBarcode.FacingIdentificationMark property

الحصول على أو تعيين نوع علامة التعريف المواجهة (FIM) المراد إدراجها.

```csharp
public string FacingIdentificationMark { get; set; }
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
