---
title: ShapeBase.ScreenTip
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. يحدد النص المعروض عندما يتحرك مؤشر الماوس فوق الشكل.
type: docs
weight: 440
url: /ar/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

يحدد النص المعروض عندما يتحرك مؤشر الماوس فوق الشكل.

```csharp
public string ScreenTip { get; set; }
```

### ملاحظات

القيمة الافتراضية هي سلسلة فارغة.

### أمثلة

يوضح كيفية إدراج شكل يحتوي على صورة ، وهو أيضًا ارتباط تشعبي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/ ";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + النقر بزر الماوس الأيسر على الشكل في Microsoft Word سيفتح نافذة متصفح ويب جديدة
// وانتقل بنا إلى الارتباط التشعبي في خاصية "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


