---
title: ShapeBase.SizeInPoints
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. الحصول على حجم الشكل بالنقاط.
type: docs
weight: 510
url: /ar/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

الحصول على حجم الشكل بالنقاط.

```csharp
public SizeF SizeInPoints { get; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


