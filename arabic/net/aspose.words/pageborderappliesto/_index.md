---
title: Enum PageBorderAppliesTo
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.PageBorderAppliesTo تعداد. يحدد الصفحات التي سيتم طباعة حدود الصفحة عليها.
type: docs
weight: 4340
url: /ar/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

يحدد الصفحات التي سيتم طباعة حدود الصفحة عليها.

```csharp
public enum PageBorderAppliesTo
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| AllPages | `0` | يظهر حد الصفحة في جميع صفحات القسم. |
| FirstPage | `1` | يظهر حد الصفحة في الصفحة الأولى من القسم فقط. |
| OtherPages | `2` | يظهر حد الصفحة في جميع الصفحات باستثناء الصفحة الأولى من القسم. |

### أمثلة

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

* class [PageSetup](../pagesetup/)
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


