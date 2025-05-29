---
title: Fill.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words لـ .NET
description: اضبط شفافية التعبئة من ٠.٠ (معتم) إلى ١.٠ (شفاف) لتأثيرات بصرية قابلة للتخصيص في تصميماتك. حسّن جمالية مشروعك اليوم!
type: docs
weight: 200
url: /ar/net/aspose.words.drawing/fill/transparency/
---
## Fill.Transparency property

يحصل على درجة شفافية التعبئة المحددة أو يعينها كقيمة بين 0.0 (غير شفاف) و1.0 (واضح).

```csharp
public double Transparency { get; set; }
```

## ملاحظات

هذه الخاصية هي عكس الخاصية[`Opacity`](../opacity/).

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
