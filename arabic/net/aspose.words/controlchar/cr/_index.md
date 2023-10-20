---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words لـ .NET
description: ControlChar Cr مجال. حرف الإرجاع x000d أو r. مثلParagraphBreak  في C#.
type: docs
weight: 50
url: /ar/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

حرف الإرجاع: "\x000d" أو "\r". مثل[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## أمثلة

يوضح كيفية استخدام أحرف التحكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإدراج فقرات تحتوي على نص باستخدام DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// يكشف تحويل المستند إلى نموذج نصي عن أحرف التحكم تلك
// تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// عند تحويل مستند إلى نموذج سلسلة،
// يمكننا حذف بعض أحرف التحكم باستخدام طريقة القطع.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### أنظر أيضا

* class [ControlChar](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
