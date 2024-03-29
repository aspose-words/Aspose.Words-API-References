---
title: Fill.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words لـ .NET
description: Fill Color ملكية. الحصول على أو تعيين كائن اللون الذي يمثل اللون الأمامي للتعبئة في C#.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing/fill/color/
---
## Fill.Color property

الحصول على أو تعيين كائن اللون الذي يمثل اللون الأمامي للتعبئة.

```csharp
public Color Color { get; set; }
```

## ملاحظات

تحافظ هذه الخاصية على مكون ألفا فيColor ‎ بخلاف[`ForeColor`](../forecolor/)الخاصية، التي تعيد تعيينه إلى لون معتم بالكامل.

## أمثلة

يوضح كيفية تحويل أي من عمليات التعبئة مرة أخرى إلى تعبئة صلبة.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// احصل على كائن التعبئة لخط التشغيل الأول.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// التحقق من خصائص التعبئة للخط.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// قم بتغيير نوع التعبئة إلى صلب بلون أخضر موحد.
fill.Solid(Color.Green);
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
