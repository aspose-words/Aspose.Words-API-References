---
title: PageSetup.BorderAppliesTo
linktitle: BorderAppliesTo
articleTitle: BorderAppliesTo
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية PageSetup BorderAppliesTo على تحسين تخطيط المستند الخاص بك عن طريق التحكم في طباعة حدود الصفحة للحصول على مظهر أنيق واحترافي.
type: docs
weight: 30
url: /ar/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

يحدد الصفحات التي سيتم طباعة حدود الصفحة عليها.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
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

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
