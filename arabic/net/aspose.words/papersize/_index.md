---
title: PaperSize Enum
linktitle: PaperSize
articleTitle: PaperSize
second_title: Aspose.Words لـ .NET
description: اكتشف مُعدّل Aspose.Words.PaperSize لتحديد أحجام ورق مخصصة في مستنداتك. حسّن تنسيق مستنداتك بسهولة!
type: docs
weight: 5110
url: /ar/net/aspose.words/papersize/
---
## PaperSize enumeration

يحدد حجم الورق.

```csharp
public enum PaperSize
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| A3 | `0` | 297 × 420 مم. |
| A4 | `1` | 210 × 297 مم. |
| A5 | `2` | 148 × 210 مم. |
| B4 | `3` | 250 × 353 مم. |
| B5 | `4` | 176 × 250 مم. |
| Executive | `5` | 7.25 × 10.5 بوصة. |
| Folio | `6` | 8.5 × 13 بوصة. |
| Ledger | `7` | 17 × 11 بوصة. |
| Legal | `8` | 8.5 × 14 بوصة. |
| Letter | `9` | 8.5 × 11 بوصة. |
| EnvelopeDL | `10` | 110 × 220 مم. |
| Quarto | `11` | 8.47 × 10.83 بوصة. |
| Statement | `12` | 8.5 × 5.5 بوصة. |
| Tabloid | `13` | 11 × 17 بوصة. |
| Paper10x14 | `14` | 10 × 14 بوصة. |
| Paper11x17 | `15` | 11 × 17 بوصة. |
| Number10Envelope | `16` | 4.125 × 9.5 بوصة. |
| JisB4 | `17` | 257 × 364 مم. |
| JisB5 | `18` | 182 × 257 مم. |
| Custom | `19` | حجم ورق مخصص. |

## أمثلة

يوضح كيفية ضبط حجم الورق والاتجاه والهوامش، إلى جانب الإعدادات الأخرى لقسم ما.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.PageSetup.PaperSize = PaperSize.Legal;
builder.PageSetup.Orientation = Orientation.Landscape;
builder.PageSetup.TopMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.BottomMargin = ConvertUtil.InchToPoint(1.0);
builder.PageSetup.LeftMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.RightMargin = ConvertUtil.InchToPoint(1.5);
builder.PageSetup.HeaderDistance = ConvertUtil.InchToPoint(0.2);
builder.PageSetup.FooterDistance = ConvertUtil.InchToPoint(0.2);

builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PageSetup.PageMargins.docx");
```

يوضح كيفية تعيين أحجام الصفحات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا تغيير حجم الصفحة الحالية إلى حجم محدد مسبقًا
// عن طريق استخدام خاصية "PaperSize" في كائن PageSetup الخاص بهذا القسم.
builder.PageSetup.PaperSize = PaperSize.Tabloid;

Assert.AreEqual(792.0d, builder.PageSetup.PageWidth);
Assert.AreEqual(1224.0d, builder.PageSetup.PageHeight);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

// لكل قسم كائن PageSetup خاص به. عند استخدام مُنشئ مستندات لإنشاء قسم جديد،
// يرث كائن PageSetup الخاص بهذا القسم جميع قيم كائن PageSetup الخاص بالقسم السابق.
builder.InsertBreak(BreakType.SectionBreakEvenPage);

Assert.AreEqual(PaperSize.Tabloid, builder.PageSetup.PaperSize);

builder.PageSetup.PaperSize = PaperSize.A5;
builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

Assert.AreEqual(419.55d, builder.PageSetup.PageWidth);
Assert.AreEqual(595.30d, builder.PageSetup.PageHeight);

builder.InsertBreak(BreakType.SectionBreakEvenPage);

// تعيين حجم مخصص لصفحات هذا القسم.
builder.PageSetup.PageWidth = 620;
builder.PageSetup.PageHeight = 480;

Assert.AreEqual(PaperSize.Custom, builder.PageSetup.PaperSize);

builder.Writeln($"This page is {builder.PageSetup.PageWidth}x{builder.PageSetup.PageHeight}.");

doc.Save(ArtifactsDir + "PageSetup.PaperSizes.docx");
```

يوضح كيفية إنشاء مستند Aspose.Words يدويًا.

```csharp
Document doc = new Document();

//تحتوي الوثيقة الفارغة على قسم واحد ونص واحد وفقرة واحدة.
//استدعاء طريقة "RemoveAllChildren" لإزالة كل هذه العقد،
// وينتهي الأمر بعقدة مستند بدون أطفال.
doc.RemoveAllChildren();

// لا تحتوي هذه الوثيقة الآن على أي عقد فرعية مركبة يمكننا إضافة محتوى إليها.
// إذا أردنا تحريره، فسوف نحتاج إلى إعادة ملء مجموعة العقد الخاصة به.
// أولاً، قم بإنشاء قسم جديد، ثم قم بإضافته كقسم فرعي إلى عقدة المستند الجذر.
Section section = new Section(doc);
doc.AppendChild(section);

// تعيين بعض خصائص إعداد الصفحة للقسم.
section.PageSetup.SectionStart = SectionStart.NewPage;
section.PageSetup.PaperSize = PaperSize.Letter;

// يحتاج القسم إلى نص، والذي سيحتوي على جميع محتوياته ويعرضها
// على الصفحة بين رأس القسم وتذييله.
Body body = new Body(doc);
section.AppendChild(body);

// قم بإنشاء فقرة، ثم اضبط بعض خصائص التنسيق، ثم أضفها كفقرة فرعية إلى النص.
Paragraph para = new Paragraph(doc);

para.ParagraphFormat.StyleName = "Heading 1";
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;

body.AppendChild(para);

// أخيرًا، أضف بعض المحتوى لإنشاء المستند. أنشئ مسارًا،
// قم بتعيين مظهره ومحتوياته، ثم قم بإضافته كطفل إلى الفقرة.
Run run = new Run(doc);
run.Text = "Hello World!";
run.Font.Color = Color.Red;
para.AppendChild(run);

Assert.AreEqual("Hello World!", doc.GetText().Trim());

doc.Save(ArtifactsDir + "Section.CreateManually.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
