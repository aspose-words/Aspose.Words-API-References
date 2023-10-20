---
title: PageSetup.Gutter
linktitle: Gutter
articleTitle: Gutter
second_title: Aspose.Words لـ .NET
description: PageSetup Gutter ملكية. الحصول على أو تعيين مقدار المساحة الإضافية المضافة إلى هامش ربط المستند في C#.
type: docs
weight: 160
url: /ar/net/aspose.words/pagesetup/gutter/
---
## PageSetup.Gutter property

الحصول على أو تعيين مقدار المساحة الإضافية المضافة إلى هامش ربط المستند.

```csharp
public double Gutter { get; set; }
```

## أمثلة

يوضح كيفية تكوين مستند يمكن طباعته كطي كتاب.

```csharp
Document doc = new Document();

// أدخل نصًا يمتد إلى 16 صفحة.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// قم بتكوين خاصية "PageSetup" للقسم الأول لطباعة المستند على شكل طية كتاب.
// عندما نطبع هذه الوثيقة على كلا الجانبين، يمكننا أخذ الصفحات لتكديسها
// وقم بطيها جميعًا في المنتصف مرة واحدة. سوف تصطف محتويات المستند في طية الكتاب.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// يمكننا فقط تحديد عدد الأوراق بمضاعفات 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

يوضح كيفية تعيين هوامش الحضيض.

```csharp
Document doc = new Document();

// أدخل نصًا يمتد على عدة صفحات.
DocumentBuilder builder = new DocumentBuilder(doc);
for (int i = 0; i < 6; i++)
{
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                  "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder.InsertBreak(BreakType.PageBreak);
}

// يضيف الحضيض مسافات بيضاء إلى هامش الصفحة الأيسر أو الأيمن،
// الذي يعوض الطي المركزي للصفحات في الكتاب الذي يتعدى على تخطيط الصفحة.
PageSetup pageSetup = doc.Sections[0].PageSetup;

// حدد مقدار المساحة المتوفرة في صفحاتنا للنص داخل الهوامش ثم أضف مقدارًا لحشو الهامش.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// اضبط خاصية "RtlGutter" على "صحيح" لوضع الهامش في موضع أكثر ملاءمة للنص من اليمين إلى اليسار.
pageSetup.RtlGutter = true;

// قم بتعيين خاصية "MultiplePages" على "MultiplePagesType.MirrorMargins" للتبديل
// موضع هوامش كل صفحة على الجانب الأيسر/الأيمن من الصفحة.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
