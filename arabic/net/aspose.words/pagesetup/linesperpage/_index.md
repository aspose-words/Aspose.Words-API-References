---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: Aspose.Words لـ .NET
description: تحكم في تخطيط مستندك باستخدام خاصية PageSetup LinesPerPage. اضبط بسهولة أسطر الصفحة لتحقيق سهولة القراءة والتنظيم الأمثل.
type: docs
weight: 240
url: /ar/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

يحصل على عدد الأسطر لكل صفحة في شبكة المستند أو يعينه.

```csharp
public int LinesPerPage { get; set; }
```

## ملاحظات

الحد الأدنى لقيمة الخاصية هو 1. تعتمد القيمة القصوى على ارتفاع الصفحة وحجم الخط في نمط Normal . الحد الأدنى لتباعد الأسطر هو 136% من حجم الخط. على سبيل المثال، الحد الأقصى لعدد الأسطر في صفحة Letter ذات هوامش بوصة واحدة هو 39.

بشكل افتراضي، تحتوي الخاصية على قيمة، حيث يكون حجم الخط أكبر بمقدار 1.5 مرة من حجم الخط الخاص بنمط Normal.

## أمثلة

يوضح كيفية تحديد حد لعدد الأسطر التي يمكن أن تحتوي عليها كل صفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتمكين العرض، ثم استخدمه لتعيين عدد الأسطر في كل صفحة في هذا القسم.
// سيؤدي حجم الخط الكبير بدرجة كافية إلى دفع بعض الأسطر إلى الأسفل إلى الصفحة التالية لتجنب تداخل الأحرف.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
