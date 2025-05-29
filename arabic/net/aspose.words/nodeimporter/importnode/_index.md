---
title: NodeImporter.ImportNode
linktitle: ImportNode
articleTitle: ImportNode
second_title: Aspose.Words لـ .NET
description: انقل العقد بسهولة بين المستندات باستخدام طريقة ImportNode من NodeImporter. حسّن سير عملك وحسّن تكامل بياناتك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

استيراد عقدة من مستند إلى آخر.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة التي سيتم استيرادها. |
| isImportChildren | Boolean | `حقيقي` لاستيراد جميع العقد الفرعية بشكل متكرر؛ وإلا،`خطأ شنيع`. |

### قيمة الإرجاع

العقدة المُستنسخة والمُستوردة. تنتمي هذه العقدة إلى مستند الوجهة، ولكن ليس لها عقدة رئيسية.

## ملاحظات

استيراد عقدة يُنشئ نسخة من العقدة المصدرية للمستند المُستورد. العقدة المُعادة ليس لها أصل. العقدة المصدرية لم تُعدّل أو تُزال من المستند الأصلي.

قبل إدراج عقدة من مستند آخر في هذا المستند، يجب استيرادها. أثناء الاستيراد، تُترجم خصائص المستند، مثل مراجع الأنماط والقوائم، من المستند الأصلي إلى المستند المُستورد. بعد استيراد العقدة، يُمكن إدراجها في المكان المناسب في المستند باستخدام[`InsertBefore`](../../compositenode/insertbefore/) أو [`InsertAfter`](../../compositenode/insertafter/).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة، فسيتم ببساطة إنشاء clone عميق للعقدة المصدر.

## أمثلة

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

        // قم بالمرور عبر جميع العقد على مستوى الكتلة في نص القسم،
        // ثم استنسخ وأدرج كل عقدة ليست الفقرة الفارغة الأخيرة في القسم.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
