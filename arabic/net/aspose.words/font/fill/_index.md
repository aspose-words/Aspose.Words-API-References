---
title: Font.Fill
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تعبئة الخط لتحسين مظهر النص الخاص بك باستخدام تنسيق التعبئة القابل للتخصيص للحصول على مظهر أنيق واحترافي.
type: docs
weight: 130
url: /ar/net/aspose.words/font/fill/
---
## Font.Fill property

يحصل على تنسيق التعبئة لـ[`Font`](../) .

```csharp
public Fill Fill { get; }
```

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

* class [Fill](../../../aspose.words.drawing/fill/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
