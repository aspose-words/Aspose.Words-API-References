---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words لـ .NET
description: ShapeBase ScreenTip ملكية. تحديد النص المعروض عندما يتحرك مؤشر الماوس فوق الشكل في C#.
type: docs
weight: 480
url: /ar/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

تحديد النص المعروض عندما يتحرك مؤشر الماوس فوق الشكل.

```csharp
public string ScreenTip { get; set; }
```

## ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

## أمثلة

يوضح كيفية إدراج شكل يحتوي على صورة، ويكون أيضًا ارتباطًا تشعبيًا.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + النقر بزر الماوس الأيسر على الشكل في Microsoft Word سيفتح نافذة متصفح ويب جديدة
// وانقلنا إلى الارتباط التشعبي الموجود في خاصية "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
