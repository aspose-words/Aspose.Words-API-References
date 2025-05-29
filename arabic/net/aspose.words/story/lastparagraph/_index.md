---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words لـ .NET
description: يمكنك الوصول إلى الفقرة الأخيرة من قصتك بسهولة باستخدام خاصية Story LastParagraph، مما يعزز تجربة إدارة السرد وتحريره.
type: docs
weight: 20
url: /ar/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

يحصل على الفقرة الأخيرة في القصة.

```csharp
public Paragraph LastParagraph { get; }
```

## أمثلة

يوضح كيفية نقل موضع مؤشر DocumentBuilder إلى عقدة محددة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// يحتوي منشئ المستندات على مؤشر يعمل كجزء من المستند
// حيث يقوم المنشئ بإضافة عقد جديدة عندما نستخدم أساليب إنشاء المستندات الخاصة به.
// يعمل هذا المؤشر بنفس الطريقة التي يعمل بها المؤشر الوامض في برنامج Microsoft Word،
// وينتهي دائمًا على الفور بعد أي عقدة أدخلها المنشئ للتو.
// لإضافة محتوى إلى جزء مختلف من المستند،
// يمكننا نقل المؤشر إلى عقدة مختلفة باستخدام طريقة "MoveTo".
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// أصبح المؤشر الآن أمام العقدة التي نقلناه إليها.
// إضافة تشغيل ثانٍ سيؤدي إلى إدراجه أمام التشغيل الأول.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// حرك المؤشر إلى نهاية المستند لمواصلة إضافة النص إلى النهاية كما في السابق.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Paragraph](../../paragraph/)
* class [Story](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
