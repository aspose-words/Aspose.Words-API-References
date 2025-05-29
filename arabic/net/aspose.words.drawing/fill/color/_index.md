---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية لون التعبئة لتخصيص لون مقدمة التصميم الخاص بك بسهولة باستخدام كائن اللون، مما يعزز الجاذبية البصرية لمشروعك.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

يحصل على كائن اللون الذي يمثل لون المقدمة للتعبئة أو يعينه.

```csharp
public Color Color { get; set; }
```

## ملاحظات

تحافظ هذه الخاصية على مكون ألفا الخاص بـColor ، على عكس[`ForeColor`](../forecolor/) الخاصية، التي تعيد تعيينها إلى لون معتم بالكامل.

## أمثلة

يوضح كيفية تحويل أي من التعبئة إلى تعبئة صلبة مرة أخرى.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// الحصول على كائن التعبئة لخط التشغيل الأول.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

//تحقق من خصائص التعبئة للخط.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// تغيير نوع التعبئة إلى صلب بلون أخضر موحد.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
