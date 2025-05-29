---
title: PageSetup.RtlGutter
linktitle: RtlGutter
articleTitle: RtlGutter
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية PageSetup RtlGutter في Microsoft Word تخطيطات الأقسام للغات التي تُكتب من اليمين إلى اليسار ومن اليسار إلى اليمين. حسّن تصميم مستندك!
type: docs
weight: 380
url: /ar/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

يحصل على أو يعين ما إذا كان Microsoft Word يستخدم المزاريب للقسم بناءً على لغة من اليمين إلى اليسار أو لغة من اليسار إلى اليمين.

```csharp
public bool RtlGutter { get; set; }
```

## أمثلة

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
