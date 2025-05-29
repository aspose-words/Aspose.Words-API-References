---
title: BorderCollection.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "ألوان مجموعة الحدود" لتخصيص وإدارة ألوان حدود تصميماتك بسهولة. حسّن واجهة المستخدم بخيارات نابضة بالحياة!
type: docs
weight: 20
url: /ar/net/aspose.words/bordercollection/color/
---
## BorderCollection.Color property

يحصل على لون الحدود أو يعينه.

```csharp
public Color Color { get; set; }
```

## ملاحظات

إرجاع لون الحد الأول في المجموعة.

تعيين لون جميع الحدود في المجموعة باستثناء الحدود القطرية.

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
