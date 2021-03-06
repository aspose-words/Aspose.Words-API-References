---
title: ImportNode
second_title: Aspose.Words لمراجع .NET API
description: يستورد عقدة من وثيقة إلى أخرى.
type: docs
weight: 20
url: /ar/net/aspose.words/nodeimporter/importnode/
---
## NodeImporter.ImportNode method

يستورد عقدة من وثيقة إلى أخرى.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcNode | Node | العقدة المراد استيرادها. |
| isImportChildren | Boolean | صحيح لاستيراد جميع العقد الفرعية بشكل متكرر ؛ خلاف ذلك ، خطأ. |

### قيمة الإرجاع

العقدة المستنسخة والمستوردة. تنتمي العقدة إلى المستند الوجهة ، ولكن ليس لها أصل.

### ملاحظات

يؤدي استيراد عقدة إلى إنشاء نسخة من العقدة المصدر تنتمي إلى المستند المستورد. العقدة التي تم إرجاعها ليس لها أصل. لم يتم تغيير عقدة المصدر أو إزالتها من المستند الأصلي.

قبل أن يتم إدراج عقدة من مستند آخر في هذا المستند ، يجب استيرادها . أثناء الاستيراد ، تتم ترجمة الخصائص الخاصة بالمستند مثل المراجع إلى الأنماط والقوائم_ من المستند الأصلي إلى مستند الاستيراد. بعد استيراد العقدة ، يمكن إدراجها في المكان المناسب في المستند باستخدام[`InsertBefore`](../../compositenode/insertbefore) أو [`InsertAfter`](../../compositenode/insertafter).

إذا كانت العقدة المصدر تنتمي بالفعل إلى المستند الوجهة ، فسيتم إنشاء نسخة عميقة من العقدة المصدر.

### أمثلة

يوضح كيفية إدراج محتويات أحد المستندات في إشارة مرجعية في مستند آخر.

```csharp
[Test]
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
/// يدخل محتويات الوثيقة بعد العقدة المحددة.
/// </summary>
static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode destinationParent = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        // حلقة خلال جميع العقد على مستوى الكتلة في جسم القسم ،
        // ثم استنساخ وأدخل كل عقدة ليست آخر فقرة فارغة من القسم.
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

* class [Node](../../node)
* class [NodeImporter](../../nodeimporter)
* مساحة الاسم [Aspose.Words](../../nodeimporter)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
