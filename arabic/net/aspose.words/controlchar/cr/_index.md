---
title: ControlChar.Cr
second_title: Aspose.Words لمراجع .NET API
description: ControlChar مجال. حرف إرجاع السطر  x000d أو  r. مثلParagraphBreak .
type: docs
weight: 50
url: /ar/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

حرف إرجاع السطر: "\ x000d" أو "\ r". مثل[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

### أمثلة

يوضح كيفية استخدام أحرف التحكم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل فقرات مع نص باستخدام DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// تحويل المستند إلى نموذج نصي يكشف عن التحكم في الأحرف
// تمثل بعض العناصر الهيكلية للمستند ، مثل فواصل الصفحات.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// عند تحويل مستند إلى شكل سلسلة ،
// يمكننا حذف بعض أحرف التحكم باستخدام طريقة Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### أنظر أيضا

* class [ControlChar](../)
* مساحة الاسم [Aspose.Words](../../controlchar/)
* المجسم [Aspose.Words](../../../)


