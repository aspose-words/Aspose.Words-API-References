---
title: PageBorderDistanceFrom Enum
linktitle: PageBorderDistanceFrom
articleTitle: PageBorderDistanceFrom
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.PageBorderDistanceFrom لتحديد حدود الصفحات بدقة. حسّن تنسيق المستند من خلال تحديد موضع الهوامش بشكل مثالي.
type: docs
weight: 5080
url: /ar/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

يحدد موضع حدود الصفحة بالنسبة لهامش الصفحة.

```csharp
public enum PageBorderDistanceFrom
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Text | `0` | يتم قياس موضع الحدود من هامش الصفحة. |
| PageEdge | `1` | يتم قياس موضع الحدود من حافة الصفحة. |

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
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
