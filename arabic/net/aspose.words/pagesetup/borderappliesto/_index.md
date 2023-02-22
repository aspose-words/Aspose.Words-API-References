---
title: PageSetup.BorderAppliesTo
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. يحدد الصفحات التي تتم طباعة حد الصفحة عليها.
type: docs
weight: 30
url: /ar/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

يحدد الصفحات التي تتم طباعة حد الصفحة عليها.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
```

### أمثلة

يوضح كيفية إنشاء حد شريط أزرق عريض أعلى الصفحة الأولى.

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
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


