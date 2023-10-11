---
title: PageSetup.CharactersPerLine
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. الحصول على أو تعيين عدد الأحرف لكل سطر في شبكة المستند.
type: docs
weight: 100
url: /ar/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

الحصول على أو تعيين عدد الأحرف لكل سطر في شبكة المستند.

```csharp
public int CharactersPerLine { get; set; }
```

### ملاحظات

الحد الأدنى لقيمة الخاصية هو 1. وتعتمد القيمة القصوى على عرض الصفحة وحجم الخط للنمط Normal . الحد الأدنى لمسافة الأحرف هو 90 بالمائة من حجم الخط. على سبيل المثال، الحد الأقصى لعدد الأحرف لكل سطر من صفحة الرسالة بهوامش مقاس بوصة واحدة هو 43.

افتراضيًا، تحتوي الخاصية على قيمة، حيث تساوي درجة الأحرف حجم الخط للنمط Normal .

### أمثلة

يوضح كيفية تحديد عدد الأحرف التي قد يحتوي عليها كل سطر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتمكين العرض، ثم استخدمه لتعيين عدد الأحرف لكل سطر في هذا القسم.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// يعتمد عدد الأحرف أيضًا على حجم الخط.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


