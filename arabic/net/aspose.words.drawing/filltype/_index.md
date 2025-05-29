---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.FillType enum لتعزيز الكائنات القابلة للتعبئة باستخدام أنواع تعبئة متعددة الاستخدامات لتحسين تصميم المستندات.
type: docs
weight: 1280
url: /ar/net/aspose.words.drawing/filltype/
---
## FillType enumeration

يحدد نوع التعبئة لكائن قابل للتعبئة.

```csharp
public enum FillType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Solid | `1` | حشوة صلبة. |
| Patterned | `2` | تعبئة منقوشة. |
| Gradient | `3` | تعبئة متدرجة. |
| Textured | `4` | حشوة محببة. |
| Background | `5` | التعبئة هي نفس الخلفية. |
| Picture | `6` | ملء الصورة. |

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
