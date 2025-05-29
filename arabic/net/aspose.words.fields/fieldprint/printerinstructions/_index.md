---
title: FieldPrint.PrinterInstructions
linktitle: PrinterInstructions
articleTitle: PrinterInstructions
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية إدارة أكواد التحكم الخاصة بالطابعة وتعليمات PostScript باستخدام FieldPrint PrinterInstructions للحصول على حلول طباعة محسّنة.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldprint/printerinstructions/
---
## FieldPrint.PrinterInstructions property

يحصل على أو يعين أحرف رمز التحكم الخاصة بالطابعة أو تعليمات PostScript.

```csharp
public string PrinterInstructions { get; set; }
```

## أمثلة

يظهر لإدراج حقل الطباعة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// يمكن لحقل الطباعة إرسال التعليمات إلى الطابعة.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// قم بتعيين المنطقة التي ستقوم الطابعة بتنفيذ التعليمات عليها.
// في هذه الحالة، ستكون الفقرة هي التي تحتوي على حقل الطباعة الخاص بنا.
field.PostScriptGroup = "para";

// عندما نستخدم طابعة تدعم PostScript لطباعة مستندنا،
// سيؤدي هذا الأمر إلى تحويل المنطقة بأكملها التي حددناها في "field.PostScriptGroup" إلى اللون الأبيض.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### أنظر أيضا

* class [FieldPrint](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
