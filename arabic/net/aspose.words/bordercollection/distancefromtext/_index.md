---
title: BorderCollection.DistanceFromText
second_title: Aspose.Words لمراجع .NET API
description: BorderCollection ملكية. الحصول على أو تعيين مسافة الحد من النص بالنقاط.
type: docs
weight: 40
url: /ar/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

الحصول على أو تعيين مسافة الحد من النص بالنقاط.

```csharp
public double DistanceFromText { get; set; }
```

### ملاحظات

الحصول على المسافة من النص للحد الأول.

يضبط المسافة من النص لجميع الحدود في المجموعة باستثناء الحدود القطرية.

ليس له أي تأثير وسيتم إعادة تعيينه تلقائيًا إلى الصفر بالنسبة لحدود خلايا الجدول.

### أمثلة

يوضح كيفية إنشاء حدود صفحة خضراء متموجة مع الظل.

```csharp
Document doc = new Document();
PageSetup pageSetup = doc.Sections[0].PageSetup;

pageSetup.Borders.LineStyle = LineStyle.DoubleWave;
pageSetup.Borders.LineWidth = 2;
pageSetup.Borders.Color = Color.Green;
pageSetup.Borders.DistanceFromText = 24;
pageSetup.Borders.Shadow = true;

doc.Save(ArtifactsDir + "PageSetup.PageBorders.docx");
```

### أنظر أيضا

* class [BorderCollection](../)
* مساحة الاسم [Aspose.Words](../../bordercollection/)
* المجسم [Aspose.Words](../../../)


