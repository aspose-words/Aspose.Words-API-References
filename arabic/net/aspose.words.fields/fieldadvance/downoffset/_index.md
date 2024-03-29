---
title: FieldAdvance.DownOffset
linktitle: DownOffset
articleTitle: DownOffset
second_title: Aspose.Words لـ .NET
description: FieldAdvance DownOffset ملكية. الحصول على أو تعيين عدد النقاط التي يجب من خلالها نقل النص الذي يلي الحقل إلى الأسفل في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldadvance/downoffset/
---
## FieldAdvance.DownOffset property

الحصول على أو تعيين عدد النقاط التي يجب من خلالها نقل النص الذي يلي الحقل إلى الأسفل.

```csharp
public string DownOffset { get; set; }
```

## أمثلة

يوضح كيفية إدراج حقل ADVANCE وتحرير خصائصه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// فيما يلي طريقتان لاستخدام حقل ADVANCE لضبط موضع النص الذي يتبعه.
// يستمر تطبيق تأثيرات حقل ADVANCE حتى تنتهي الفقرة،
// أو حقل ADVANCE آخر يقوم بتحديث قيم الإزاحة/الإحداثيات.
// 1 - تحديد إزاحة الاتجاه:
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

// 2 - نقل النص إلى الموضع المحدد بالإحداثيات:
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
