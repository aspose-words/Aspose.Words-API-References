---
title: Class NodeCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.NodeCollection فصل. يمثل مجموعة من العقد من نوع معين.
type: docs
weight: 3960
url: /ar/net/aspose.words/nodecollection/
---
## NodeCollection class

يمثل مجموعة من العقد من نوع معين.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | الحصول على عدد العقد في المجموعة. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | استرداد عقدة في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل كافة العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | لتحديد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | إرجاع الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | إدراج عقدة في المجموعة بالفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | يزيل العقدة من المجموعة ومن الوثيقة. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | يزيل العقدة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | ينسخ كل العقد من المجموعة إلى مصفوفة جديدة من العقد. |

### ملاحظات

**NodeCollection** لا تمتلك العقد التي تحتوي عليها ، بل هي مجرد مجموعة مختارة من العقد_ من النوع المحدد ، ولكن يتم تخزين العقد في الشجرة تحت العقد الأصلية الخاصة بها.

**NodeCollection**يدعم الوصول المفهرس والتكرار ويوفر طرق الإضافة والإزالة.

ال **NodeCollection** المجموعة "مباشرة" ، أي التغييرات التي تم إجراؤها على العناصر الفرعية للعقدة object التي تم إنشاؤها منها تنعكس على الفور في العقد التي يتم إرجاعها بواسطة **NodeCollection** الخصائص والأساليب.

**NodeCollection** تم إرجاعه بواسطة[`GetChildNodes`](../compositenode/getchildnodes/) ويعمل أيضًا كفئة أساسية لمجموعات العقد المكتوبة مثل[`SectionCollection`](../sectioncollection/) ، [`ParagraphCollection`](../paragraphcollection/) إلخ.

**NodeCollection** يمكن أن تكون "مسطحة" وتحتوي فقط على توابع مباشرة للعقدة التي تم إنشاؤها_ منها ، أو يمكن أن تكون "عميقة" وتحتوي على جميع التوابع التابعة.

### أمثلة

يوضح كيفية استبدال جميع أشكال مربع النص بأشكال الصور.

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

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


