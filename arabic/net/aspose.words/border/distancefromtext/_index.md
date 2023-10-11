---
title: Border.DistanceFromText
second_title: Aspose.Words لمراجع .NET API
description: Border ملكية. الحصول على أو تعيين مسافة الحد من النص أو من حافة الصفحة بالنقاط.
type: docs
weight: 20
url: /ar/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

الحصول على أو تعيين مسافة الحد من النص أو من حافة الصفحة بالنقاط.

```csharp
public double DistanceFromText { get; set; }
```

### ملاحظات

ليس له أي تأثير وسيتم إعادة تعيينه تلقائيًا إلى الصفر بالنسبة لحدود خلايا الجدول.

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

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../border/)
* المجسم [Aspose.Words](../../../)


