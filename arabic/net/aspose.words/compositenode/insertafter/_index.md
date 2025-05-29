---
title: CompositeNode.InsertAfter
linktitle: InsertAfter
articleTitle: InsertAfter
second_title: Aspose.Words لـ .NET
description: قم بإدراج العقد بسهولة باستخدام طريقة CompositeNode InsertAfter، مما يعمل على تحسين إدارة بنية البيانات لديك وضمان وضع العقد بكفاءة.
type: docs
weight: 150
url: /ar/net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter&lt;T&gt; method

يقوم بإدراج العقدة المحددة فورًا بعد عقدة المرجع المحددة.

```csharp
public T InsertAfter<T>(T newChild, Node refChild)
    where T : Node
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| newChild | T | ال[`Node`](../../node/) لإدراج. |
| refChild | Node | ال[`Node`](../../node/) هذه هي العقدة المرجعية.*newChild* يتم وضعه بعد*refChild*. |

### قيمة الإرجاع

العقدة المدرجة.

## ملاحظات

لو*refChild* يكون`باطل` ، إدراجات*newChild* في بداية قائمة العقد الفرعية.

إذا كان*newChild* إذا كان موجودًا بالفعل في الشجرة، فيجب إزالته أولاً.

إذا تم إنشاء العقدة التي يتم إدراجها من مستند آخر، فيجب عليك استخدام [`ImportNode`](../../documentbase/importnode/) لاستيراد العقدة إلى المستند الحالي. يمكن بعد ذلك إدراج العقدة المستوردة في المستند الحالي.

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

يوضح كيفية إضافة وتحديث وحذف العقد الفرعية في مجموعة CompositeNode الفرعية.

```csharp
Document doc = new Document();

// تحتوي الوثيقة الفارغة، بشكل افتراضي، على فقرة واحدة.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// يمكن للعقد المركبة مثل فقرتنا أن تحتوي على عقد مركبة ومضمنة أخرى كأبناء.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// إنشاء ثلاث عقد تشغيل أخرى.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// لن يعرض نص المستند هذه العمليات حتى نقوم بإدخالها في عقدة مركبة
// وهذا في حد ذاته جزء من شجرة عقدة المستند، كما فعلنا في التشغيل الأول.
// يمكننا تحديد مكان محتوى النص للعقد التي نقوم بإدراجها
// يظهر في المستند عن طريق تحديد موقع الإدراج بالنسبة لعقدة أخرى في الفقرة.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

//أدخل التشغيل الثاني في الفقرة الموجودة أمام التشغيل الأولي.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

//أدخل التشغيل الثالث بعد التشغيل الأولي.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// قم بإدراج التشغيل الأول في بداية مجموعة العقد الفرعية للفقرة.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

//يمكننا تعديل محتويات التشغيل عن طريق تحرير وحذف العقد الفرعية الموجودة.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### أنظر أيضا

* class [Node](../../node/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
