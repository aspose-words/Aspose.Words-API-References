---
title: Paragraph.IsEndOfSection
linktitle: IsEndOfSection
articleTitle: IsEndOfSection
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Paragraph IsEndOfSection، وحدد ما إذا كانت الفقرة هي الأخيرة في النص الرئيسي للقسم لتحسين بنية المستند ووضوحه.
type: docs
weight: 80
url: /ar/net/aspose.words/paragraph/isendofsection/
---
## Paragraph.IsEndOfSection property

صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في[`Body`](../../body/) (قصة النص الرئيسي) لـ[`Section`](../../section/) ؛ وإلا فسيكون خاطئًا.

```csharp
public bool IsEndOfSection { get; }
```

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

* class [Paragraph](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
