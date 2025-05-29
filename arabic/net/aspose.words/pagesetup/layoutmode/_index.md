---
title: PageSetup.LayoutMode
linktitle: LayoutMode
articleTitle: LayoutMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup LayoutMode لتخصيص تخطيط مستندك بسهولة. حسّن تصميمك بخيارات أقسام مرنة!
type: docs
weight: 190
url: /ar/net/aspose.words/pagesetup/layoutmode/
---
## PageSetup.LayoutMode property

يحصل على وضع تخطيط هذا القسم أو يعينه.

```csharp
public SectionLayoutMode LayoutMode { get; set; }
```

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

* enum [SectionLayoutMode](../../sectionlayoutmode/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
