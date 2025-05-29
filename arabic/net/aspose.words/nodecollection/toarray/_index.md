---
title: NodeCollection.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة NodeCollection ToArray، وقم بتحويل مجموعة العقد الخاصة بك إلى مصفوفة جديدة بسهولة، مما يعزز إدارة البيانات وإمكانية الوصول إليها.
type: docs
weight: 110
url: /ar/net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

نسخ جميع العقد من المجموعة إلى مجموعة جديدة من العقد.

```csharp
public Node[] ToArray()
```

### قيمة الإرجاع

مجموعة من العقد.

## ملاحظات

لا يجب عليك إضافة/إزالة العقد أثناء التكرار عبر مجموعة من العقد لأن ذلك يبطل عمل المتكرر ويتطلب تحديثات للمجموعات الحية.

لتتمكن من إضافة/إزالة العقد أثناء التكرار، استخدم هذه الطريقة لنسخ عقد إلى مصفوفة ذات حجم ثابت ثم التكرار عبر المصفوفة.

## أمثلة

يوضح كيفية استبدال كافة أشكال مربع النص بأشكال الصور.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### أنظر أيضا

* class [Node](../../node/)
* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
