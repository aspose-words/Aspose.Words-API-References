---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CompositeNode GetChild لاسترداد عقدة الطفل Nth من نوع معين بسهولة، مما يعزز كفاءة إدارة البيانات لديك.
type: docs
weight: 100
url: /ar/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

يعيد عقدة فرعية رقم N تطابق النوع المحدد.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| nodeType | NodeType | يحدد نوع العقدة الفرعية. |
| index | Int32 | مؤشر يعتمد على الصفر للعقدة الفرعية التي يجب تحديدها. يُسمح أيضًا بالمؤشرات السلبية وتشير إلى الوصول من النهاية، أي -1 تعني العقدة الأخيرة. |
| isDeep | Boolean | `حقيقي` لتحديد من جميع العقد الفرعية بشكل متكرر؛ `خطأ شنيع` للاختيار فقط من بين الأبناء المباشرين. راجع الملاحظات لمزيد من المعلومات. |

### قيمة الإرجاع

العقدة الفرعية التي تطابق المعايير أو`باطل` إذا لم يتم العثور على عقدة مطابقة.

## ملاحظات

إذا كان المؤشر خارج النطاق،`باطل` تم إرجاعه.

لاحظ أن عقد العلامات (StructuredDocumentTag وSmartTag ) يتم اجتيازها حتى عندما*isDeep* =`خطأ شنيع` و`GetChild` يتم استدعاؤه لنوع العقدة غير الترميزية. على سبيل المثال، إذا تم تغليف التشغيل الأول في para بـ[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) ، سيتم إرجاعه مرة أخرى`GetChild`(Run ، 0،`خطأ شنيع`).

## أمثلة

يوضح كيفية تطبيق خصائص نمط الجدول مباشرة على عناصر الجدول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

//تتعلق هذه الطريقة بخصائص نمط الجدول مثل تلك التي قمنا بتعيينها أعلاه.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
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

### أنظر أيضا

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
