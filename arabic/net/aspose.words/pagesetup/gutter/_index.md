---
title: PageSetup.Gutter
linktitle: Gutter
articleTitle: Gutter
second_title: Aspose.Words لـ .NET
description: اضبط إعدادات PageSetup Gutter لتحسين هوامش المستندات للتجليد. حسّن تصميمك بهوامش مثالية لنتائج احترافية.
type: docs
weight: 160
url: /ar/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

يحصل على مقدار المساحة الإضافية المضافة إلى الهامش لربط المستند أو يعينه.

```csharp
public double Gutter { get; set; }
```

## أمثلة

يوضح كيفية تكوين مستند يمكن طباعته ككتاب مطوي.

```csharp
Document doc = new Document();

//إدراج نص يمتد على 16 صفحة.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// قم بتكوين خاصية "PageSetup" في القسم الأول لطباعة المستند في شكل كتاب مطوي.
// عندما نقوم بطباعة هذه الوثيقة على كلا الجانبين، يمكننا أخذ الصفحات لتكديسها
// ثم اطوِها كلها من المنتصف دفعةً واحدة. سيُطوى محتوى المستند ككتاب.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// يمكننا فقط تحديد عدد الأوراق بمضاعفات 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

يوضح كيفية ضبط هوامش الميزاب.

```csharp
Document doc = new Document();

//إدراج نص يمتد على عدة صفحات.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// يضيف الميزاب مسافات بيضاء إلى هامش الصفحة الأيسر أو الأيمن،
// وهو ما يعوض عن طي الصفحات في منتصف الكتاب مما يتعدى على تخطيط الصفحة.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // حدد مقدار المساحة المتوفرة في صفحاتنا للنص داخل الهوامش ثم أضف مقدارًا لتبطين الهامش.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// قم بضبط خاصية "RtlGutter" على "true" لوضع الحافة في موضع أكثر ملاءمة للنص من اليمين إلى اليسار.
pageSetup.RtlGutter = true;

// اضبط خاصية "MultiplePages" على "MultiplePagesType.MirrorMargins" للتبديل
// موضع الهوامش على الجانب الأيسر/الأيمن من الصفحة في كل صفحة.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
