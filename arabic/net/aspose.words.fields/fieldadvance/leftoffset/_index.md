---
title: FieldAdvance.LeftOffset
linktitle: LeftOffset
articleTitle: LeftOffset
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldAdvance LeftOffset لضبط محاذاة النص بسهولة من خلال تحديد نقاط للحركة الدقيقة إلى اليسار. حسّن تصميم مستندك!
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldadvance/leftoffset/
---
## FieldAdvance.LeftOffset property

يحصل على عدد النقاط التي يجب أن يتحرك بها النص الذي يلي الحقل إلى اليسار أو يعينه.

```csharp
public string LeftOffset { get; set; }
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
