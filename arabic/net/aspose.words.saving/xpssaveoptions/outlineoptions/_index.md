---
title: XpsSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية XpsSaveOptions OutlineOptions لتخصيص إعدادات مخطط مستندك لتحسين التنظيم والعرض.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/xpssaveoptions/outlineoptions/
---
## XpsSaveOptions.OutlineOptions property

يسمح بتحديد خيارات المخطط التفصيلي.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## ملاحظات

لاحظ أن[`ExpandedOutlineLevels`](../../outlineoptions/expandedoutlinelevels/) لن يعمل الخيار عند الحفظ في XPS.

## أمثلة

يوضح كيفية تحديد مستوى العناوين التي ستظهر في مخطط مستند XPS المحفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل العناوين التي يمكن أن تكون بمثابة إدخالات جدول المحتويات للمستويات 1، 2، ثم 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// قم بإنشاء كائن "XpsSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// سيحتوي مستند XPS الناتج على مخطط تفصيلي، وهو جدول محتويات يسرد العناوين الموجودة في نص المستند.
// النقر على إدخال في هذا المخطط سيأخذنا إلى موقع العنوان الخاص به.
// قم بضبط خاصية "HeadingsOutlineLevels" على "2" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 2 من المخطط التفصيلي.
// لن يظهر آخر عنوانين قمنا بإدخالهما أعلاه.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### أنظر أيضا

* class [OutlineOptions](../../outlineoptions/)
* class [XpsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
