---
title: PageSetup.BorderDistanceFrom
linktitle: BorderDistanceFrom
articleTitle: BorderDistanceFrom
second_title: Aspose.Words لـ .NET
description: PageSetup BorderDistanceFrom ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كان حد الصفحة المحدد يتم قياسه من حافة الصفحة أو من النص المحيط بها في C#.
type: docs
weight: 40
url: /ar/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

الحصول على أو تعيين قيمة تشير إلى ما إذا كان حد الصفحة المحدد يتم قياسه من حافة الصفحة أو من النص المحيط بها.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
```

## أمثلة

يوضح كيفية إنشاء حد شريطي أزرق عريض في أعلى الصفحة الأولى.

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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
