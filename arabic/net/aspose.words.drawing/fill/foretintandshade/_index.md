---
title: Fill.ForeTintAndShade
linktitle: ForeTintAndShade
articleTitle: ForeTintAndShade
second_title: Aspose.Words لـ .NET
description: قم بضبط خاصية ForeTintAndShade لتفتيح أو تعتيم لون المقدمة بسهولة، مما يعزز تصميمك بدقة وإبداع.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/fill/foretintandshade/
---
## Fill.ForeTintAndShade property

يحصل على قيمة مزدوجة أو يعينها لتفتيح أو تعتيم لون المقدمة.

```csharp
public double ForeTintAndShade { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | قم بالرمي إذا قمت بتعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1. |

## ملاحظات

القيم المسموح بها تتراوح من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية.

الصفر (0) محايد.

## أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
