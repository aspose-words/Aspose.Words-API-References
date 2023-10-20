---
title: NodeImporter
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words لـ .NET
description: NodeImporter البناء. تهيئة مثيل جديد لـNodeImporter فئة في C#.
type: docs
weight: 10
url: /ar/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/)*) {#constructor}

تهيئة مثيل جديد لـ[`NodeImporter`](../) فئة.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | DocumentBase | الوثيقة المصدر. |
| dstDoc | DocumentBase | مستند الوجهة الذي سيكون مالك العقد المستوردة. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات النمط التي تتعارض. |

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

* class [DocumentBase](../../documentbase/)
* enum [ImportFormatMode](../../importformatmode/)
* class [NodeImporter](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## NodeImporter(*[DocumentBase](../../documentbase/), [DocumentBase](../../documentbase/), [ImportFormatMode](../../importformatmode/), [ImportFormatOptions](../../importformatoptions/)*) {#constructor_1}

تهيئة مثيل جديد لـ[`NodeImporter`](../) فئة.

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | DocumentBase | الوثيقة المصدر. |
| dstDoc | DocumentBase | مستند الوجهة الذي سيكون مالك العقد المستوردة. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيقات النمط التي تتعارض. |
| importFormatOptions | ImportFormatOptions | يحدد خيارات متنوعة لتنسيق العقدة المستوردة. |

## أمثلة

يوضح كيفية حل التعارض عند استيراد المستندات التي تحتوي على قوائم بنفس معرف تعريف القائمة.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// قم بتعيين خاصية "KeepSourceNumbering" على "صحيح" لتطبيق معرف تعريف قائمة مختلف
// إلى أنماط متطابقة عندما يقوم Aspose.Words باستيرادها إلى المستندات الوجهة.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

يوضح كيفية حل تضارب ترقيم القائمة في المستندات المصدر والوجهة.

```csharp
// افتح مستندًا بنظام ترقيم قائمة مخصص، ثم انسخه.
// نظرًا لأن كلاهما لهما نفس تنسيق الترقيم، فسوف تتعارض التنسيقات إذا قمنا باستيراد مستند واحد إلى الآخر.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// عندما نستورد نسخة المستند إلى المستند الأصلي ثم نلحقه،
// ثم ستنضم القائمتان بنفس تنسيق القائمة.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" على "خطأ"، فسيتم استنساخ القائمة من المستند
// الذي نلحقه بالأصل سيستمر في ترقيم القائمة التي نلحقها بها.
// سيؤدي هذا إلى دمج القائمتين بشكل فعال في قائمة واحدة.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" على "صحيح"، فسيتم استنساخ المستند
 // ستحتفظ القائمة بترقيمها الأصلي، مما يجعل القائمتين تظهران كقوائم منفصلة.
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
