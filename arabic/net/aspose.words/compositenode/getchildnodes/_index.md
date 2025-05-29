---
title: CompositeNode.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CompositeNode GetChildNodes—استرجاع مجموعة حية من العقد الفرعية المصممة خصيصًا لنوعك المحدد لتحسين الأداء.
type: docs
weight: 110
url: /ar/net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

يعيد مجموعة حية من العقد الفرعية التي تطابق النوع المحدد.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| nodeType | NodeType | يحدد نوع العقد المراد تحديدها. |
| isDeep | Boolean | `حقيقي` لتحديد من جميع العقد الفرعية بشكل متكرر؛ `خطأ شنيع` للاختيار فقط من بين الأطفال المباشرين. |

### قيمة الإرجاع

مجموعة حية من العقد الفرعية من النوع المحدد.

## ملاحظات

إن مجموعة العقد التي تم إرجاعها بواسطة هذه الطريقة تكون دائمًا حية.

المجموعة الحية متزامنة دائمًا مع المستند. على سبيل المثال، إذا قمتَ بتحديد جميع أقسام مستند، ثم حذفتَ الأقسام من خلال المجموعة، فسيتم حذف القسم من المجموعة فورًا بعد إزالته من المستند.

## أمثلة

يوضح كيفية طباعة كافة تعليقات المستند وردودها.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);
// إذا لم يكن للتعليق سلف، فهو تعليق "على مستوى أعلى" وليس تعليق من نوع الرد.
// اطبع جميع التعليقات ذات المستوى الأعلى بالإضافة إلى أي ردود قد تكون لديهم.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

يوضح كيفية استخراج الصور من مستند وحفظها في نظام الملفات المحلي كملفات فردية.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// الحصول على مجموعة الأشكال من المستند،
// وحفظ بيانات الصورة لكل شكل مع الصورة كملف في نظام الملفات المحلي.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // قد تحتوي بيانات الصورة الخاصة بالأشكال على صور بتنسيقات صور متعددة محتملة.
        // يمكننا تحديد امتداد الملف لكل صورة تلقائيًا، استنادًا إلى تنسيقها.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

يوضح كيفية التنقل عبر مجموعة العقد الفرعية للعقدة المركبة.

```csharp
Document doc = new Document();

// أضف تشغيلتين وشكلًا واحدًا كعقد فرعية إلى الفقرة الأولى من هذه الوثيقة.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// لاحظ أن 'CustomNodeId' لا يتم حفظه في ملف إخراج ولا يوجد إلا أثناء عمر العقدة.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// قم بالتكرار خلال مجموعة الأطفال المباشرين للفقرة،
// وطباعة أي مسارات أو أشكال نجدها بالداخل.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
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

* class [NodeCollection](../../nodecollection/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
