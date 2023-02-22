---
title: Story.LastParagraph
second_title: Aspose.Words لمراجع .NET API
description: Story ملكية. الحصول على آخر فقرة في القصة .
type: docs
weight: 20
url: /ar/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

الحصول على آخر فقرة في القصة .

```csharp
public Paragraph LastParagraph { get; }
```

### أمثلة

يوضح كيفية نقل موضع مؤشر DocumentBuilder إلى عقدة محددة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// يحتوي مُنشئ المستند على مؤشر يعمل كجزء من المستند
// حيث يقوم المنشئ بإلحاق عقد جديدة عندما نستخدم طرق إنشاء المستندات الخاصة به.
// يعمل هذا المؤشر بنفس طريقة عمل مؤشر Microsoft Word الوامض ،
// ودائمًا ما ينتهي به الأمر فورًا بعد أي عقدة قام المنشئ بإدراجها للتو.
// لإلحاق المحتوى بجزء مختلف من المستند ،
// يمكننا تحريك المؤشر إلى عقدة مختلفة باستخدام طريقة "MoveTo".
// يوجد المؤشر الآن أمام العقدة التي نقلناها إليها.
// ستؤدي إضافة تشغيل ثانٍ إلى إدراجه أمام التشغيل الأول.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// حرك المؤشر إلى نهاية المستند لمتابعة إلحاق النص بالنهاية كما كان من قبل.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Paragraph](../../paragraph/)
* class [Story](../)
* مساحة الاسم [Aspose.Words](../../story/)
* المجسم [Aspose.Words](../../../)


