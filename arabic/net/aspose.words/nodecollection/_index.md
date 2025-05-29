---
title: NodeCollection Class
linktitle: NodeCollection
articleTitle: NodeCollection
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.NodeCollection، الحل الأمثل لإدارة أنواع العقد المتنوعة بكفاءة في معالجة المستندات. حسّن سير عملك اليوم!
type: docs
weight: 4890
url: /ar/net/aspose.words/nodecollection/
---
## NodeCollection class

يمثل مجموعة من العقد من نوع معين.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | يحصل على عدد العقد في المجموعة. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | يسترجع عقدة عند الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | يضيف عقدة إلى نهاية المجموعة. |
| [Clear](../../aspose.words/nodecollection/clear/)() | يزيل جميع العقد من هذه المجموعة ومن المستند. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | يحدد ما إذا كانت العقدة موجودة في المجموعة. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | يوفر تكرارًا بسيطًا بأسلوب "foreach" عبر مجموعة العقد. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | يعيد الفهرس المبني على الصفر للعقدة المحددة. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | يقوم بإدراج عقدة في المجموعة عند الفهرس المحدد. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | يزيل العقدة من المجموعة ومن المستند. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | يزيل العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | نسخ جميع العقد من المجموعة إلى مجموعة جديدة من العقد. |

## ملاحظات

`NodeCollection` لا يمتلك العقد التي يحتويها، بل هو مجرد مجموعة مختارة من nodes من النوع المحدد، ولكن يتم تخزين العقد في الشجرة أسفل العقد الأصلية الخاصة بها.

`NodeCollection` يدعم الوصول المفهرس والتكرار ويوفر طرق الإضافة والإزالة.

ال`NodeCollection` المجموعة "حية"، أي أن التغييرات التي تطرأ على أبناء العقدة object التي تم إنشاؤها منها تنعكس على الفور في العقد التي تم إرجاعها بواسطة`NodeCollection` خصائص وطرق .

`NodeCollection` يتم إرجاعه بواسطة[`GetChildNodes`](../compositenode/getchildnodes/) ويعمل أيضًا كفئة أساسية لمجموعات العقد المكتوبة مثل[`SectionCollection`](../sectioncollection/) ، [`ParagraphCollection`](../paragraphcollection/) إلخ.

`NodeCollection`يمكن أن يكون "مسطحًا" ويحتوي فقط على أبناء مباشرين للعقدة التي تم إنشاؤه منها ، أو يمكن أن يكون "عميقًا" ويحتوي على جميع الأطفال المنحدرين.

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

* class [Node](../node/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
