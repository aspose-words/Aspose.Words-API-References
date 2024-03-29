---
title: BorderCollection.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words لـ .NET
description: BorderCollection Shadow ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كان الحد يحتوي على ظل في C#.
type: docs
weight: 110
url: /ar/net/aspose.words/bordercollection/shadow/
---
## BorderCollection.Shadow property

الحصول على أو تعيين قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.

```csharp
public bool Shadow { get; set; }
```

## ملاحظات

الحصول على القيمة من الحد الأول في المجموعة.

يضبط القيمة لجميع الحدود في المجموعة باستثناء الحدود القطرية.

## أمثلة

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
