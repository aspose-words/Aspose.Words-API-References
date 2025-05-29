---
title: Paragraph.JoinRunsWithSameFormatting
linktitle: JoinRunsWithSameFormatting
articleTitle: JoinRunsWithSameFormatting
second_title: Aspose.Words لـ .NET
description: اجمع عمليات التشغيل بسهولة بتنسيق متسق في فقراتك باستخدام طريقة JoinRunsWithSameFormatting. حسّن أسلوب مستندك اليوم!
type: docs
weight: 300
url: /ar/net/aspose.words/paragraph/joinrunswithsameformatting/
---
## Paragraph.JoinRunsWithSameFormatting method

ينضم إلى التشغيلات بنفس التنسيق في الفقرة.

```csharp
public int JoinRunsWithSameFormatting()
```

### قيمة الإرجاع

عدد عمليات الانضمام التي تم إجراؤها. عندما**ن** يتم ضم الجولات المتجاورة، ويتم احتسابها على أنها**ن - 1** ينضم.

## أمثلة

يوضح كيفية تبسيط الفقرات عن طريق دمج الفقرات غير الضرورية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أدخل أربعة سلاسل من النص في الفقرة.
builder.Write("Run 1. ");
builder.Write("Run 2. ");
builder.Write("Run 3. ");
builder.Write("Run 4. ");

// إذا فتحنا هذا المستند في Microsoft Word، ستبدو الفقرة وكأنها نص واحد مترابط.
// ومع ذلك، سيتكون من أربع عمليات تشغيل منفصلة بنفس التنسيق. فقرات مجزأة مثل هذه
// قد يحدث هذا عندما نقوم يدويًا بتحرير أجزاء من فقرة واحدة عدة مرات في Microsoft Word.
Paragraph para = builder.CurrentParagraph;

Assert.AreEqual(4, para.Runs.Count);

// قم بتغيير نمط التشغيل الأخير لتمييزه عن التشغيلات الثلاثة الأولى.
para.Runs[3].Font.StyleIdentifier = StyleIdentifier.Emphasis;

// يمكننا تشغيل طريقة "JoinRunsWithSameFormatting" لتحسين محتويات المستند
// عن طريق دمج عمليات التشغيل المتشابهة في عملية واحدة، مما يقلل من عددها الإجمالي.
// تقوم هذه الطريقة أيضًا بإرجاع عدد عمليات التشغيل التي تم دمجها بهذه الطريقة.
// حدث هذان الدمجان لدمج الجولات رقم 1 و2 و3،
// مع ترك Run #4 خارجًا لأنه يحتوي على نمط غير متوافق.
Assert.AreEqual(2, para.JoinRunsWithSameFormatting());

// عدد الجولات المتبقية سوف يساوي العدد الأصلي
// ناقص عدد عمليات الدمج التي تم تنفيذها بواسطة طريقة "JoinRunsWithSameFormatting".
Assert.AreEqual(2, para.Runs.Count);
Assert.AreEqual("Run 1. Run 2. Run 3. ", para.Runs[0].Text);
Assert.AreEqual("Run 4. ", para.Runs[1].Text);
```

### أنظر أيضا

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
