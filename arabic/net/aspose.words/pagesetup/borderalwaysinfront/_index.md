---
title: PageSetup.BorderAlwaysInFront
linktitle: BorderAlwaysInFront
articleTitle: BorderAlwaysInFront
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup BorderAlwaysInFront لتحسين حدود الصفحة وتعزيز التخطيط والرؤية للنصوص والكائنات المتقاطعة.
type: docs
weight: 20
url: /ar/net/aspose.words/pagesetup/borderalwaysinfront/
---
## PageSetup.BorderAlwaysInFront property

يحدد مكان وضع حدود الصفحة بالنسبة للنصوص والكائنات المتقاطعة.

```csharp
public bool BorderAlwaysInFront { get; set; }
```

## أمثلة

يوضح كيفية إنشاء حدود ذات شريط أزرق عريض في الجزء العلوي من الصفحة الأولى.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### أنظر أيضا

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
