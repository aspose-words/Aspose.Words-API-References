---
title: Node Class
linktitle: Node
articleTitle: Node
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Node فصل. الفئة الأساسية لجميع العقد في مستند Word في C#.
type: docs
weight: 4170
url: /ar/net/aspose.words/node/
---
## Node class

الفئة الأساسية لجميع العقد في مستند Word.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public abstract class Node
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصصة. |
| virtual [Document](../../aspose.words/node/document/) { get; } | الحصول على المستند الذي تنتمي إليه هذه العقدة. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة يمكن أن تحتوي على عقد أخرى. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | يحصل على نوع هذه العقدة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الأصل المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرة. |
| [Range](../../aspose.words/node/range/) { get; } | إرجاع أ[`Range`](../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل الزائر. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | إنشاء نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للمحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor_1)(*Type*) | الحصول على السلف الأول لنوع الكائن المحدد. |
| virtual [GetText](../../aspose.words/node/gettext/)() | الحصول على نص هذه العقدة وجميع أبنائها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*Node*) | الحصول على العقدة التالية وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*Node*) | الحصول على العقدة السابقة وفقًا لخوارزمية اجتياز شجرة الطلب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/#tostring_1)(*[SaveFormat](../saveformat/)*) | تصدير محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/#tostring_2)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | تصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(*[NodeType](../nodetype/)*) | طريقة مساعدة تقوم بتحويل قيمة تعداد نوع العقدة إلى سلسلة سهلة الاستخدام. |

## ملاحظات

يتم تمثيل المستند كشجرة من العقد، تشبه DOM أو XmlDocument.

لمزيد من المعلومات، راجع نمط التصميم المركب.

ال`Node` فصل:

* يحدد واجهة العقدة الفرعية.
* يحدد الواجهة لزيارة العقد.
* يوفر إمكانية الاستنساخ الافتراضية.
* ينفذ العقدة الأصلية وآليات وثيقة المالك.
* ينفذ الوصول إلى العقد الأخوة.

## أمثلة

يوضح كيفية إزالة جميع العقد الفرعية من نوع معين من العقدة المركبة.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // احفظ العقدة الشقيقة التالية كمتغير في حالة أردنا الانتقال إليها بعد حذف هذه العقدة.
    Node nextNode = curNode.NextSibling;

    // يمكن أن يحتوي نص القسم على عقد الفقرة والجدول.
    // إذا كانت العقدة عبارة عن جدول، فقم بإزالتها من الأصل.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

يوضح كيفية استنساخ عقدة مركبة.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// فيما يلي طريقتان لاستنساخ عقدة مركبة.
// 1 - أنشئ نسخة من العقدة، وأنشئ نسخة من كل عقد من العقد التابعة لها أيضًا.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - إنشاء نسخة من العقدة بمفردها دون أي عناصر فرعية.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
