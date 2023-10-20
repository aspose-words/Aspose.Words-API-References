---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words لـ .NET
description: Aspose.Words.SectionLayoutMode تعداد. يحدد وضع التخطيط لقسم يسمح بتحديد سلوك شبكة الوثيقة في C#.
type: docs
weight: 5750
url: /ar/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

يحدد وضع التخطيط لقسم يسمح بتحديد سلوك شبكة الوثيقة.

```csharp
public enum SectionLayoutMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Default | `0` | يحدد عدم تطبيق أي شبكة مستند على محتويات القسم المقابل في المستند. |
| Grid | `1` | يحدد أن القسم المقابل يجب أن يحتوي على كل من درجة الخط الإضافية ودرجة الأحرف المضافة إلى كل سطر وحرف داخله من أجل الحفاظ على عدد محدد من الأسطر لكل صفحة والأحرف لكل سطر. لن تتم محاذاة الأحرف تلقائيًا مع خطوط الشبكة على الكتابة. |
| LineGrid | `2` | يحدد أن القسم المقابل يجب أن يحتوي على خطوة إضافية للخط تضاف إلى كل سطر بداخله من أجل الحفاظ على عدد الأسطر المحدد لكل صفحة. |
| SnapToChars | `3` | يحدد أن القسم المقابل يجب أن يحتوي على كل من درجة الخط الإضافية ودرجة الأحرف المضافة إلى كل سطر وحرف داخله من أجل الحفاظ على عدد معين من الأسطر لكل صفحة والأحرف لكل سطر. ستتم محاذاة الأحرف تلقائيًا مع خطوط الشبكة عند الكتابة. |

## أمثلة

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

يوضح كيفية تحديد حد لعدد الأسطر التي قد تحتوي عليها كل صفحة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتمكين العرض، ثم استخدمه لتعيين عدد الأسطر لكل صفحة في هذا القسم.
// سيؤدي حجم الخط الكبير بدرجة كافية إلى دفع بعض الأسطر لأسفل إلى الصفحة التالية لتجنب تداخل الأحرف.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
