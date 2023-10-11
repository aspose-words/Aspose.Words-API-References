---
title: CompositeNode.GetChild
second_title: Aspose.Words لمراجع .NET API
description: CompositeNode طريقة. إرجاع العقدة الفرعية N التي تطابق النوع المحدد.
type: docs
weight: 100
url: /ar/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

إرجاع العقدة الفرعية N التي تطابق النوع المحدد.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| nodeType | NodeType | يحدد نوع العقدة الفرعية. |
| index | Int32 | الفهرس الصفري للعقدة الفرعية المراد تحديده. يُسمح أيضًا بالفهارس السالبة وتشير إلى الوصول من النهاية، الذي يعني -1 العقدة الأخيرة. |
| isDeep | Boolean | `حقيقي` للاختيار من بين جميع العقد الفرعية بشكل متكرر؛ `خطأ شنيع`للاختيار فقط بين الأطفال المباشرين. انظر الملاحظات لمزيد من المعلومات. |

### قيمة الإرجاع

العقدة الفرعية التي تطابق المعايير أو`باطل` إذا لم يتم العثور على عقدة مطابقة.

### ملاحظات

إذا كان الفهرس خارج النطاق، أ`باطل` يتم إرجاع.

لاحظ أن العقد الترميزية (StructuredDocumentTag وSmartTag ) يتم اجتيازها حتى عندما*isDeep* =`خطأ شنيع` و`GetChild` يتم استدعاؤه لنوع العقدة غير الترميزية. على سبيل المثال، إذا تم تغليف التشغيل الأول في para بملف a[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) ، سيتم إعادته بواسطة`GetChild`(Run , 0,`خطأ شنيع`).

### أمثلة

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

// تتعلق هذه الطريقة بخصائص نمط الجدول مثل تلك التي حددناها أعلاه.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

يوضح كيفية اجتياز مجموعة العقد الفرعية للعقدة المركبة.

```csharp
Document doc = new Document();

// أضف مسارين وشكلًا واحدًا كعقد فرعية إلى الفقرة الأولى من هذه الوثيقة.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// لاحظ أن "CustomNodeId" لا يتم حفظه في ملف إخراج وهو موجود فقط أثناء عمر العقدة.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// كرر من خلال مجموعة الفقرة من العناصر الفرعية المباشرة،
// وطباعة أي مسارات أو أشكال نجدها داخلها.
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
* مساحة الاسم [Aspose.Words](../../compositenode/)
* المجسم [Aspose.Words](../../../)


