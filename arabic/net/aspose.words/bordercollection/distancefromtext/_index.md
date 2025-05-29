---
title: BorderCollection.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BorderCollection DistanceFromText لتخصيص مسافات حدود النص بسهولة في تصميماتك. حسّن تصميمك بسهولة!
type: docs
weight: 40
url: /ar/net/aspose.words/bordercollection/distancefromtext/
---
## BorderCollection.DistanceFromText property

يحصل على أو يعين مسافة الحدود من النص بالنقاط.

```csharp
public double DistanceFromText { get; set; }
```

## ملاحظات

يحصل على المسافة من النص للحد الأول.

تعيين المسافة من النص لجميع الحدود في المجموعة باستثناء الحدود القطرية.

ليس له أي تأثير وسيتم إعادة تعيينه تلقائيًا إلى الصفر بالنسبة لحدود خلايا الجدول.

## أمثلة

يوضح كيفية إنشاء حدود صفحة متموجة باللون الأخضر مع ظل.

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
