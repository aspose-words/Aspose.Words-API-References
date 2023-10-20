---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words لـ .NET
description: PageSetup RtlGutter ملكية. الحصول على أو تعيين ما إذا كان Microsoft Word يستخدم المزاريب للقسم بناءً على لغة من اليمين إلى اليسار أو لغة من اليسار إلى اليمين في C#.
type: docs
weight: 380
url: /ar/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

الحصول على أو تعيين ما إذا كان Microsoft Word يستخدم المزاريب للقسم بناءً على لغة من اليمين إلى اليسار أو لغة من اليسار إلى اليمين.

```csharp
public bool RtlGutter { get; set; }
```

## أمثلة

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
