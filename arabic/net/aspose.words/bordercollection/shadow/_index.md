---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ظلال BorderCollection لتحسين تصميماتك. تحكم بسهولة في ظلال الحدود لإضفاء مظهر عصري وأنيق على مشاريعك!
type: docs
weight: 110
url: /ar/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كانت الحدود تحتوي على ظل.

```csharp
public bool Shadow { get; set; }
```

## ملاحظات

يحصل على القيمة من الحد الأول في المجموعة.

تعيين القيمة لجميع الحدود في المجموعة باستثناء الحدود القطرية.

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
