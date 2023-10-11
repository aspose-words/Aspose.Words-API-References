---
title: Fill.ForeTintAndShade
second_title: Aspose.Words لمراجع .NET API
description: Fill ملكية. الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح أو تغميق اللون الأمامي.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح أو تغميق اللون الأمامي.

```csharp
public double ForeTintAndShade { get; set; }
```

### ملاحظات

القيم المسموح بها تقع ضمن النطاق من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية. الصفر (0) محايد. محاولة تعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1 تؤدي إلىArgumentOutOfRangeException.

### أمثلة

يوضح كيفية إدارة تفتيح وتغميق لون الخط الأمامي.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

Fill textFill = doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Fill;
textFill.ForeThemeColor = ThemeColor.Accent1;
if (textFill.ForeTintAndShade == 0)
    textFill.ForeTintAndShade = 0.5;

doc.Save(ArtifactsDir + "Shape.FillTintAndShade.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../fill/)
* المجسم [Aspose.Words](../../../)


