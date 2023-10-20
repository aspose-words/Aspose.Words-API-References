---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words لـ .NET
description: Paragraph JoinRunsWithSameFormatting طريقة. يتم تشغيل عمليات الانضمام بنفس التنسيق في الفقرة في C#.
type: docs
weight: 280
url: /ar/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

يتم تشغيل عمليات الانضمام بنفس التنسيق في الفقرة.

```csharp
public int JoinRunsWithSameFormatting()
```

### قيمة الإرجاع

عدد الصلات التي تم تنفيذها. متى**ن** يتم ضم الأشواط المجاورة التي يتم احتسابها**ن - 1** ينضم.

## أمثلة

يوضح كيفية تبسيط الفقرات عن طريق دمج عمليات التشغيل الزائدة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل أربعة أجزاء من النص في الفقرة.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// إذا فتحنا هذا المستند في برنامج Microsoft Word، فستبدو الفقرة كنص نصي واحد سلس.
// ومع ذلك، سيتكون من أربع عمليات تشغيل منفصلة بنفس التنسيق. فقرات مجزأة مثل هذا
// قد يحدث عندما نقوم بتحرير أجزاء من فقرة واحدة يدويًا عدة مرات في Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// قم بتغيير نمط الجولة الأخيرة لتمييزها عن الثلاثة الأولى.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// يمكننا تشغيل طريقة "JoinRunsWithSameFormatting" لتحسين محتويات المستند
// من خلال دمج عمليات التشغيل المتشابهة في عملية واحدة، مما يؤدي إلى تقليل العدد الإجمالي لها.
// تقوم هذه الطريقة أيضًا بإرجاع عدد عمليات التشغيل التي تم دمجها بهذه الطريقة.
// حدث هذان الدمجان لدمج العمليات رقم 1 ورقم 2 ورقم 3،
// أثناء ترك التشغيل رقم 4 لأنه يحتوي على نمط غير متوافق.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// عدد مرات التشغيل المتبقية سوف يساوي العدد الأصلي
// ناقص عدد عمليات الدمج التي نفذتها طريقة "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
