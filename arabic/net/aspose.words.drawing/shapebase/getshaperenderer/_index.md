---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ShapeBase GetShapeRenderer لإنشاء الأشكال وتقديمها كصور بسهولة، مما يعزز مشاريع التصميم الخاصة بك بسهولة.
type: docs
weight: 670
url: /ar/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

ينشئ ويعيد كائنًا يمكن استخدامه لتحويل هذا الشكل إلى صورة.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### قيمة الإرجاع

كائن العرض لهذا الشكل.

## ملاحظات

هذه الطريقة تستدعي فقط[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) المنشئ ويمرر هذا الكائن كمعلمة.

## أمثلة

يوضح كيفية استخدام برنامج عرض الأشكال لتصدير الأشكال إلى ملفات في نظام الملفات المحلي.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// يوجد 7 أشكال في المستند، بما في ذلك شكل مجموعة واحد مع شكلين فرعيين.
// سنقوم بتحويل كل شكل إلى ملف صورة في نظام الملفات المحلي
// مع تجاهل أشكال المجموعة لأنها ليس لها مظهر.
// سيؤدي هذا إلى إنتاج 6 ملفات صور.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### أنظر أيضا

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
