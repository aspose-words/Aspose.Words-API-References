---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ShapeBase SizeInPoints لاسترداد أبعاد الشكل بالنقاط وإدارتها بسهولة للتحكم الدقيق في التصميم.
type: docs
weight: 540
url: /ar/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

يحصل على حجم الشكل بالنقاط.

```csharp
public SizeF SizeInPoints { get; }
```

## أمثلة

يوضح كيفية التحقق من حجم الشكل ولغة الترميز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
