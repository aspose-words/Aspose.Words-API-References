---
title: XpsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words لـ .NET
description: XpsSaveOptions SaveFormat ملكية. يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقطXps  في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/xpssaveoptions/saveformat/
---
## XpsSaveOptions.SaveFormat property

يحدد التنسيق الذي سيتم حفظ المستند به في حالة استخدام كائن خيارات الحفظ هذا. يمكن أن يكون فقطXps .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## أمثلة

يوضح كيفية تحديد مستوى العناوين التي ستظهر في المخطط التفصيلي لمستند XPS المحفوظ.

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

// قم بإنشاء كائن "XpsSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذا الأسلوب للمستند إلى .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// سيحتوي مستند XPS الناتج على مخطط تفصيلي، وجدول محتويات يسرد العناوين في نص المستند.
// سيؤدي النقر فوق أحد الإدخالات في هذا المخطط إلى نقلنا إلى موقع العنوان الخاص به.
// قم بتعيين خاصية "HeadingsOutlineLevels" على "2" لاستبعاد جميع العناوين التي تكون مستوياتها أعلى من 2 من المخطط التفصيلي.
// لن يظهر العنوانان الأخيران اللذان أدخلناهما أعلاه.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### أنظر أيضا

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [XpsSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
