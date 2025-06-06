---
title: PageSetup.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup Borders للوصول بسهولة إلى حدود صفحتك وتخصيصها للحصول على مظهر أنيق واحترافي في مستنداتك.
type: docs
weight: 50
url: /ar/net/aspose.words/pagesetup/borders/
---
## PageSetup.Borders property

يحصل على مجموعة من حدود الصفحة.

```csharp
public BorderCollection Borders { get; }
```

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

* class [BorderCollection](../../bordercollection/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
