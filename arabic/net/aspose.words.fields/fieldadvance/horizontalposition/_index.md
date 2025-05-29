---
title: FieldAdvance.HorizontalPosition
linktitle: HorizontalPosition
articleTitle: HorizontalPosition
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldAdvance HorizontalPosition، واضبط موضع النص بسهولة للتحكم الدقيق في تخطيط مستنداتك. حسّن تنسيقك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldadvance/horizontalposition/
---
## FieldAdvance.HorizontalPosition property

يحصل على أو يعين عدد النقاط التي يجب نقل النص الذي يتبع الحقل أفقيًا من الحافة اليسرى للعمود أو الإطار أو مربع النص.

```csharp
public string HorizontalPosition { get; set; }
```

## أمثلة

يوضح كيفية إدراج حقل ADVANCE وتحرير خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// فيما يلي طريقتان لاستخدام الحقل ADVANCE لتعديل موضع النص الذي يليه.
// تستمر تأثيرات حقل ADVANCE في التطبيق حتى نهاية الفقرة،
// أو يقوم حقل ADVANCE آخر بتحديث قيم الإزاحة/الإحداثيات.
// 1 - تحديد الإزاحة الاتجاهية:
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

// 2 - نقل النص إلى موضع محدد بواسطة الإحداثيات:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### أنظر أيضا

* class [FieldAdvance](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
