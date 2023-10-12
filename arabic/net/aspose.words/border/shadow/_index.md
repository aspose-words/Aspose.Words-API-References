---
title: Border.Shadow
second_title: Aspose.Words لمراجع .NET API
description: Border ملكية. الحصول على أو تعيين قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.
type: docs
weight: 60
url: /ar/net/aspose.words/border/shadow/
---
## Border.Shadow property

الحصول على أو تعيين قيمة تشير إلى ما إذا كان الحد يحتوي على ظل.

```csharp
public bool Shadow { get; set; }
```

### ملاحظات

في Microsoft Word، لكي يكون للحدود ظل، يجب أن تكون الحدود على الجوانب الأربعة (اليسار والأعلى واليمين والأسفل) من نفس النوع والعرض واللون ويجب أن تحتوي جميعها على خاصية الظل المعينة على`حقيقي`.

### أمثلة

يوضح كيفية إنشاء حدود صفحة خضراء متموجة مع الظل.

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

* class [Border](../)
* مساحة الاسم [Aspose.Words](../../border/)
* المجسم [Aspose.Words](../../../)


