---
title: ShapeBase.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase Target لتعيين أو استرداد إطارات هدف الارتباط التشعبي بسهولة لأشكالك، مما يعزز تنقل المستخدم وتجربته.
type: docs
weight: 560
url: /ar/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

يحصل على إطار الهدف لرابط الشكل التشعبي أو يعينه.

```csharp
public string Target { get; set; }
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
