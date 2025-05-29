---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.PageBorderAppliesTo للتحكم في طباعة حدود الصفحة عبر صفحات محددة لتحسين تنسيق المستندات.
type: docs
weight: 5070
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
| AllPages | `0` | يتم عرض حدود الصفحة في جميع صفحات القسم. |
| FirstPage | `1` | يتم عرض حدود الصفحة في الصفحة الأولى من القسم فقط. |
| OtherPages | `2` | يتم عرض حدود الصفحة في جميع الصفحات باستثناء الصفحة الأولى من القسم. |

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

* class [PageSetup](../pagesetup/)
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
