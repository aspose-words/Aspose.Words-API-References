---
title: NodeImporter
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words لـ .NET
description: اكتشف منشئ NodeImporter، وقم بإنشاء مثيلات NodeImporter جديدة بسهولة لتبسيط إدارة البيانات لديك وتعزيز كفاءة المشروع.
type: docs
weight: 10
url: /ar/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/)*) {#constructor}

يقوم بتهيئة مثيل جديد لـ[`NodeImporter`](../) الصف.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | DocumentBase | الوثيقة المصدرية. |
| dstDoc | DocumentBase | المستند الوجهة الذي سيكون مالكًا للعقد المستوردة. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات الأنماط المتعارضة. |

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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#constructor_1}

يقوم بتهيئة مثيل جديد لـ[`NodeImporter`](../) الصف.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | DocumentBase | الوثيقة المصدرية. |
| dstDoc | DocumentBase | المستند الوجهة الذي سيكون مالكًا للعقد المستوردة. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات الأنماط المتعارضة. |
| importFormatOptions | ImportFormatOptions | يحدد خيارات مختلفة لتنسيق العقدة المستوردة. |

## أمثلة

يوضح كيفية حل التعارض عند استيراد المستندات التي تحتوي على قوائم بنفس معرف تعريف القائمة.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// اضبط خاصية "KeepSourceNumbering" على "true" لتطبيق معرف تعريف قائمة مختلف
// إلى الأنماط المتطابقة مثل Aspose.Words التي يستوردها إلى المستندات الوجهة.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

يوضح كيفية حل تعارضات ترقيم القائمة في المستندات المصدر والوجهة.

```csharp
// افتح مستندًا يحتوي على مخطط ترقيم قائمة مخصص، ثم استنسخه.
// نظرًا لأن كلاهما لهما نفس تنسيق الترقيم، فسوف تتعارض التنسيقات إذا قمنا باستيراد مستند واحد إلى الآخر.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// عندما نقوم باستيراد نسخة من المستند إلى المستند الأصلي ثم إضافته،
// ثم سيتم دمج القائمتين اللتين لهما نفس تنسيق القائمة.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" إلى "false"، فسيتم استنساخ القائمة من المستند
// الذي نضيفه إلى الأصل سيحمل ترقيم القائمة التي نضيفه إليها.
// سيؤدي هذا إلى دمج القائمتين في قائمة واحدة بشكل فعال.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" إلى "true"، فسيتم استنساخ المستند
 // ستحافظ القائمة على ترقيمها الأصلي، مما يجعل القائمتين تظهران كقوائم منفصلة.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### أنظر أيضا

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [NodeImporter](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
