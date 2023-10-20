---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words لـ .NET
description: FieldPrint PostScriptGroup ملكية. الحصول على أو تعيين مستطيل الرسم الذي تعمل عليه تعليمات PostScript في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

الحصول على أو تعيين مستطيل الرسم الذي تعمل عليه تعليمات PostScript.

```csharp
public string PostScriptGroup { get; set; }
```

## أمثلة

يظهر لإدراج حقل طباعة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// يمكن لحقل الطباعة إرسال تعليمات إلى الطابعة.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// قم بتعيين المنطقة للطابعة لتنفيذ التعليمات.
// في هذه الحالة، ستكون الفقرة هي التي تحتوي على حقل الطباعة الخاص بنا.
field.PostScriptGroup = "para";

// عندما نستخدم طابعة تدعم PostScript لطباعة وثيقتنا،
// سيحول هذا الأمر المنطقة بأكملها التي حددناها في "field.PostScriptGroup" إلى اللون الأبيض.
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### أنظر أيضا

* class [FieldPrint](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
