---
title: Border.DistanceFromText
linktitle: DistanceFromText
articleTitle: DistanceFromText
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Border DistanceFromText لضبط مسافة الحدود بسهولة من النص أو حواف الصفحة بالنقاط لتحسين التحكم في التخطيط.
type: docs
weight: 20
url: /ar/net/aspose.words/border/distancefromtext/
---
## Border.DistanceFromText property

يحصل على أو يعين مسافة الحدود من النص أو من حافة الصفحة بالنقاط.

```csharp
public double DistanceFromText { get; set; }
```

## ملاحظات

ليس له أي تأثير وسيتم إعادة تعيينه تلقائيًا إلى الصفر بالنسبة لحدود خلايا الجدول.

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

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
