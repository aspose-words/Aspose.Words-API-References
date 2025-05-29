---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words لـ .NET
description: اكتشف ControlChar Cr، حرف الإرجاع (x000d أو r) الذي يُحسّن تنسيق النص. بسّط برمجة أعمالك مع حلولنا الفريدة!
type: docs
weight: 50
url: /ar/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

حرف إرجاع العربة: "\x000d" أو "\r". نفس[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## أمثلة

يوضح كيفية استخدام أحرف التحكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج فقرات تحتوي على نص باستخدام DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// يؤدي تحويل المستند إلى نموذج نصي إلى إظهار أن أحرف التحكم
// تمثل بعض العناصر الهيكلية للمستند، مثل فواصل الصفحات.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// عند تحويل مستند إلى شكل سلسلة،
// يمكننا حذف بعض أحرف التحكم باستخدام طريقة Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### أنظر أيضا

* class [ControlChar](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
