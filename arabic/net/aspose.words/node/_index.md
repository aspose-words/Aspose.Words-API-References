---
title: Node Class
linktitle: Node
articleTitle: Node
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Node، الأساس الضروري لجميع عقد مستندات Word، مما يتيح معالجة المستندات وتخصيصها بشكل سلس.
type: docs
weight: 4860
url: /ar/net/aspose.words/node/
---
## Node class

الفئة الأساسية لجميع عقد مستند Word.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public abstract class Node
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | يحدد معرف العقدة المخصص. |
| virtual [Document](../../aspose.words/node/document/) { get; } | يحصل على المستند الذي تنتمي إليه هذه العقدة. |
| virtual [IsComposite](../../aspose.words/node/iscomposite/) { get; } | إرجاع`حقيقي` إذا كانت هذه العقدة قادرة على احتواء عقد أخرى. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | يحصل على العقدة التي تلي هذه العقدة مباشرة. |
| abstract [NodeType](../../aspose.words/node/nodetype/) { get; } | يحصل على نوع هذه العقدة. |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | يحصل على الوالد المباشر لهذه العقدة. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | يحصل على العقدة التي تسبق هذه العقدة مباشرةً. |
| [Range](../../aspose.words/node/range/) { get; } | يعيد[`Range`](../range/)الكائن الذي يمثل الجزء من المستند الموجود في هذه العقدة. |

## طُرق

| اسم | وصف |
| --- | --- |
| abstract [Accept](../../aspose.words/node/accept/)(*[DocumentVisitor](../documentvisitor/)*) | يقبل زائرًا. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | ينشئ نسخة مكررة من العقدة. |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor)(*[NodeType](../nodetype/)*) | يحصل على السلف الأول للعنصر المحدد[`NodeType`](../nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/#getancestor_1)(*Type*) | يحصل على السلف الأول لنوع الكائن المحدد. |
| virtual [GetText](../../aspose.words/node/gettext/)() | يحصل على نص هذه العقدة وجميع أبنائها. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*Node*) | يحصل على العقدة التالية وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*Node*) | يحصل على العقدة السابقة وفقًا لخوارزمية عبور شجرة الترتيب المسبق. |
| [Remove](../../aspose.words/node/remove/)() | يزيل نفسه من الأصل. |
| [ToString](../../aspose.words/node/tostring/#tostring_1)(*[SaveFormat](../saveformat/)*) | يصدر محتوى العقدة إلى سلسلة بالتنسيق المحدد. |
| [ToString](../../aspose.words/node/tostring/#tostring_2)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | يقوم بتصدير محتوى العقدة إلى سلسلة باستخدام خيارات الحفظ المحددة. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(*[NodeType](../nodetype/)*) | طريقة مساعدة تقوم بتحويل قيمة عددية لنوع العقدة إلى سلسلة سهلة الاستخدام. |

## ملاحظات

يتم تمثيل المستند كشجرة من العقد، على غرار DOM أو XmlDocument.

لمزيد من المعلومات راجع نمط التصميم المركب.

ال`Node` فصل:

* يحدد واجهة العقدة الفرعية.
* يحدد الواجهة لزيارة العقد.
* يوفر إمكانية الاستنساخ الافتراضية.
* تنفيذ آليات وثيقة العقدة الأصلية والمالك.
* تنفيذ الوصول إلى العقد الشقيقة.

## أمثلة

يوضح كيفية إزالة جميع العقد الفرعية من نوع معين من عقدة مركبة.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // احفظ العقدة الشقيقة التالية كمتغير في حالة أردنا الانتقال إليها بعد حذف هذه العقدة.
    Node nextNode = curNode.NextSibling;

    // يمكن أن يحتوي نص القسم على عقد الفقرات والجداول.
    // إذا كانت العقدة عبارة عن جدول، قم بإزالتها من العقدة الأصلية.
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
// 1 - قم بإنشاء نسخة طبق الأصل من عقدة، ثم قم بإنشاء نسخة طبق الأصل من كل عقدة فرعية لها أيضًا.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - إنشاء نسخة طبق الأصل من العقدة بمفردها دون أي أطفال.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
