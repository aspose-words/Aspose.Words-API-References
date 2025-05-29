---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words لـ .NET
description: تحكم في تخطيط مستندك باستخدام خاصية PageSetup CharactersPerLine. اضبط بسهولة الأحرف في كل سطر لضمان سهولة القراءة والتصميم الأمثل.
type: docs
weight: 100
url: /ar/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

يحصل على عدد الأحرف لكل سطر في شبكة المستند أو يعينه.

```csharp
public int CharactersPerLine { get; set; }
```

## ملاحظات

الحد الأدنى لقيمة الخاصية هو 1. تعتمد القيمة القصوى على عرض الصفحة وحجم الخط في نمط Normal . الحد الأدنى لتباعد الأحرف هو 90% من حجم الخط. على سبيل المثال، الحد الأقصى لعدد الأحرف في كل سطر في صفحة Letter ذات هوامش بوصة واحدة هو 43 حرفًا.

بشكل افتراضي، تحتوي الخاصية على قيمة، حيث يكون حجم الحرف مساويًا لحجم الخط في النمط Normal .

## أمثلة

يوضح كيفية تحديد عدد الأحرف التي يمكن أن يحتوي عليها كل سطر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتمكين العرض، ثم استخدمه لتعيين عدد الأحرف لكل سطر في هذا القسم.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

//يعتمد عدد الأحرف أيضًا على حجم الخط.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
