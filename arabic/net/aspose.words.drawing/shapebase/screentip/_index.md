---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase ScreenTip، وقم بتحسين تجربة المستخدم من خلال تخصيص نص التلميح الذي يظهر عند تحريك الماوس فوق الأشكال.
type: docs
weight: 510
url: /ar/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

يحدد النص المعروض عند تحرك مؤشر الماوس فوق الشكل.

```csharp
public string ScreenTip { get; set; }
```

## ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

## أمثلة

يوضح كيفية إدراج شكل يحتوي على صورة، وهو أيضًا ارتباط تشعبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// الضغط على Ctrl + النقر بزر الماوس الأيسر على الشكل في Microsoft Word سيؤدي إلى فتح نافذة متصفح ويب جديدة
// ويأخذنا إلى الرابط التشعبي في خاصية "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
