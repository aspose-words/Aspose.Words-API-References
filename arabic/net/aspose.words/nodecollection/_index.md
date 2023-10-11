---
title: Class NodeCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.NodeCollection فصل. يمثل مجموعة من العقد من نوع معين.
type: docs
weight: 4200
url: /ar/net/aspose.words/nodecollection/
---
## NodeCollection class

يمثل مجموعة من العقد من نوع معين.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | الحصول على عدد العقد في المجموعة. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | يسترد عقدة في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | إضافة عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | إزالة كافة العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | تحديد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا لنمط "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | إرجاع الفهرس الصفري للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | إدراج عقدة في المجموعة في الفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | إزالة العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | إزالة العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | نسخ كافة العقد من المجموعة إلى مجموعة جديدة من العقد. |

### ملاحظات

`NodeCollection` لا يمتلك العقد التي يحتوي عليها، بل هو مجرد مجموعة مختارة من العقد من النوع المحدد، ولكن يتم تخزين العقد في الشجرة تحت العقد الأصلية الخاصة بها.

`NodeCollection`يدعم الوصول المفهرس والتكرار ويوفر طرق الإضافة والإزالة.

ال`NodeCollection` المجموعة "مباشرة"، أي أن التغييرات التي يتم إجراؤها على العناصر الفرعية للعقدة object التي تم إنشاؤها منها تنعكس فورًا في العقد التي يتم إرجاعها بواسطة`NodeCollection` الخصائص والأساليب.

`NodeCollection` يتم إرجاعها بواسطة[`GetChildNodes`](../compositenode/getchildnodes/) ويعمل أيضًا كفئة أساسية لمجموعات العقدة المكتوبة مثل[`SectionCollection`](../sectioncollection/)[`ParagraphCollection`](../paragraphcollection/) إلخ.

`NodeCollection` يمكن أن تكون "مسطحة" وتحتوي فقط على العناصر الفرعية المباشرة للعقدة التي تم إنشاؤها منها، أو يمكن أن تكون "عميقة" وتحتوي على جميع العناصر الفرعية.

### أمثلة

يوضح كيفية استبدال جميع أشكال مربعات النص بأشكال الصور.

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


