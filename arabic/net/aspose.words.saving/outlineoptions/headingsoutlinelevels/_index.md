---
title: OutlineOptions.HeadingsOutlineLevels
second_title: Aspose.Words لمراجع .NET API
description: OutlineOptions ملكية. يحدد عدد مستويات العناوين الفقرات المنسقة باستخدام أنماط العناوين التي سيتم تضمينها في مخطط المستند .
type: docs
weight: 70
url: /ar/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

يحدد عدد مستويات العناوين (الفقرات المنسقة باستخدام أنماط العناوين) التي سيتم تضمينها في مخطط المستند .

```csharp
public int HeadingsOutlineLevels { get; set; }
```

### ملاحظات

حدد 0 لعدم وجود عناوين في المخطط التفصيلي؛ حدد 1 لمستوى واحد من العناوين في المخطط التفصيلي وهكذا.

الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

### أمثلة

يوضح كيفية تحويل مستند كامل إلى PDF بثلاثة مستويات في مخطط المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل عناوين المستويات من 1 إلى 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// سيحتوي مستند PDF الناتج على مخطط تفصيلي، وهو عبارة عن جدول محتويات يسرد العناوين في نص المستند.
// سيؤدي النقر فوق أحد الإدخالات في هذا المخطط إلى نقلنا إلى موقع العنوان الخاص به.
// قم بتعيين خاصية "HeadingsOutlineLevels" على "4" لاستبعاد كافة العناوين التي تكون مستوياتها أعلى من 4 من المخطط التفصيلي.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// إذا كان الإدخال التفصيلي يحتوي على إدخالات لاحقة بمستوى أعلى بينه وبين الإدخال التالي من نفس المستوى أو مستوى أقل،
// سيظهر سهم على يسار الإدخال. هذا الإدخال هو "مالك" العديد من هذه "الإدخالات الفرعية".
// في مستندنا، إدخالات المخطط التفصيلي من مستوى العنوان الخامس هي إدخالات فرعية لإدخال المخطط التفصيلي للمستوى الرابع الثاني،
// إدخالات مستوى العنوان الرابع والخامس هي إدخالات فرعية لإدخال المستوى الثالث الثاني، وهكذا.
// في المخطط التفصيلي، يمكننا النقر على سهم إدخال "المالك" لطي/توسيع جميع إدخالاته الفرعية.
// قم بتعيين خاصية "ExpandedOutlineLevels" على "2" لتوسيع كل مستوى العناوين 2 وإدخالات المخطط التفصيلي السفلية تلقائيًا
// وقم بطي جميع المستويات والإدخالات الثلاثة والأعلى عندما نفتح المستند.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### أنظر أيضا

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../outlineoptions/)
* المجسم [Aspose.Words](../../../)


