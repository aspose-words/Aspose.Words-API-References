---
title: NodeImporter.ImportNode
second_title: Aspose.Words لمراجع .NET API
description: NodeImporter طريقة. يستورد عقدة من مستند إلى آخر.
type: docs
weight: 20
url: /ar/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

يستورد عقدة من مستند إلى آخر.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة المراد استيرادها. |
| isImportChildren | Boolean | `حقيقي` لاستيراد كافة العقد التابعة بشكل متكرر؛ خلاف ذلك،`خطأ شنيع`. |

### قيمة الإرجاع

العقدة المستنسخة والمستوردة. تنتمي العقدة إلى المستند الوجهة، ولكن ليس لها أصل.

### ملاحظات

يؤدي استيراد عقدة إلى إنشاء نسخة من العقدة المصدر التي تنتمي إلى مستند الاستيراد. العقدة التي تم إرجاعها ليس لها أصل. لا يتم تغيير العقدة المصدر أو إزالتها من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تتم ترجمة الخصائص الخاصة بالمستند مثل المراجع إلى الأنماط والقوائم من المستند الأصلي إلى مستند الاستيراد. بعد استيراد العقدة، يمكن إدراجها في المكان المناسب في المستند باستخدامNode) أو Node).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء استنساخ عميق للعقدة المصدر.

### أمثلة

يوضح كيفية إدراج محتويات مستند واحد في إشارة مرجعية في مستند آخر.

```csharp
public void InsertAtBookmark()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("InsertionPoint");
    builder.Write("We will insert a document here: ");
    builder.EndBookmark("InsertionPoint");

    Document docToInsert = new Document();
    builder = new DocumentBuilder(docToInsert);

    builder.Write("Hello world!");

    docToInsert.Save(ArtifactsDir + "NodeImporter.InsertAtMergeField.docx");

    Bookmark bookmark = doc.Range.Bookmarks["InsertionPoint"];
    InsertDocument(bookmark.BookmarkStart.ParentNode, docToInsert);

    Assert.AreEqual("We will insert a document here: " +
                    "\rHello world!", doc.GetText().Trim());
}

/// <summary>
/// إدراج محتويات المستند بعد العقدة المحددة.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // قم بالتكرار عبر جميع العقد على مستوى الكتلة في نص القسم،
        // ثم انسخ وأدخل كل عقدة ليست آخر فقرة فارغة في القسم.
        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                destinationParent.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node should be either a paragraph or table.");
    }
}
```

### أنظر أيضا

* class [Node](../../node/)
* class [NodeImporter](../)
* مساحة الاسم [Aspose.Words](../../nodeimporter/)
* المجسم [Aspose.Words](../../../)


