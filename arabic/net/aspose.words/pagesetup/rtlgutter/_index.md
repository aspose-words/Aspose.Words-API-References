---
title: RtlGutter
second_title: Aspose.Words لمراجع .NET API
description: الحصول على أو تحديد ما إذا كان Microsoft Word يستخدم المزاريب للقسم بناءً على لغة من اليمين إلى اليسار أو لغة من اليسار إلى اليمين.
type: docs
weight: 370
url: /ar/net/aspose.words/pagesetup/rtlgutter/
---
## PageSetup.RtlGutter property

الحصول على أو تحديد ما إذا كان Microsoft Word يستخدم المزاريب للقسم بناءً على لغة من اليمين إلى اليسار أو لغة من اليسار إلى اليمين.

```csharp
public bool RtlGutter { get; set; }
```

### أمثلة

يوضح كيفية تعيين هوامش هامش التوثيق.

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

// يضيف الحضيض مسافات بيضاء إلى هامش الصفحة الأيمن أو الأيسر ،
// مما يعوض عن طي الوسط للصفحات في كتاب يتعدى على تخطيط الصفحة.
PageSetup pageSetup = doc.Sections[0].PageSetup;

 // حدد مقدار المساحة المتوفرة لصفحاتنا للنص داخل الهوامش ثم أضف مقدارًا لتضمين الهامش.
Assert.AreEqual(470.30d, pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin, 0.01d);

pageSetup.Gutter = 100.0d;

// اضبط خاصية "RtlGutter" على "true" لوضع هامش التوثيق في موضع أكثر ملاءمة للنص من اليمين إلى اليسار.
pageSetup.RtlGutter = true;

// اضبط خاصية "MultiplePages" على "MultiplePagesType.MirrorMargins" على البديل
// موضع جانب الصفحة الأيسر / الأيمن للهوامش لكل صفحة.
pageSetup.MultiplePages = MultiplePagesType.MirrorMargins;

doc.Save(ArtifactsDir + "PageSetup.Gutter.docx");
```

### أنظر أيضا

* class [PageSetup](../../pagesetup)
* مساحة الاسم [Aspose.Words](../../pagesetup)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->