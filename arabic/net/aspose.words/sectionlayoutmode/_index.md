---
title: Enum SectionLayoutMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.SectionLayoutMode تعداد. يحدد وضع التخطيط لقسم يسمح بتعريف سلوك شبكة الوثيقة.
type: docs
weight: 5460
url: /ar/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

يحدد وضع التخطيط لقسم يسمح بتعريف سلوك شبكة الوثيقة.

```csharp
public enum SectionLayoutMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Default | `0` | يحدد عدم تطبيق أي شبكة مستندات على محتويات القسم المقابل في المستند. |
| Grid | `1` | يحدد أن القسم المقابل يجب أن يحتوي على كل من خطوة الخط الإضافية والحرف_ملاحظة مضافًا إلى كل سطر وحرف بداخله من أجل الحفاظ على عدد معين_ من الأسطر في الصفحة والأحرف في كل سطر. _ لن يتم محاذاة الأحرف تلقائيًا مع خطوط الشبكة على كتابة . |
| LineGrid | `2` | يحدد أن القسم المقابل يجب أن يكون لديه خطوة خط إضافية مضافة إلى كل سطر داخل it من أجل الحفاظ على العدد المحدد من الأسطر لكل صفحة. |
| SnapToChars | `3` | يحدد أن القسم المقابل يجب أن يحتوي على كل من خطوة السطر الإضافية والحرف Pitch مضافًا إلى كل سطر وحرف بداخله من أجل الحفاظ على عدد معين_ من الأسطر في الصفحة والأحرف في كل سطر. ستتم محاذاة الأحرف تلقائيًا مع خطوط الشبكة عند الكتابة. |

### أمثلة

يوضح كيفية تحديد عدد الأحرف التي قد يحتوي عليها كل سطر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتمكين التدوير ، ثم استخدمه لتعيين عدد الأحرف في كل سطر في هذا القسم.
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

// تمكين الترويج ، ثم استخدمه لتعيين عدد الأسطر لكل صفحة في هذا القسم.
// سيؤدي حجم الخط الكبير بدرجة كافية إلى دفع بعض الأسطر لأسفل في الصفحة التالية لتجنب تداخل الأحرف.
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


