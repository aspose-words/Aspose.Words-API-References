---
title: NodeImporter
second_title: Aspose.Words لمراجع .NET API
description: يقوم بتهيئة مثيل جديد لملفNodeImporteraspose.words/nodeimporter فئة ._ x000d_
type: docs
weight: 10
url: /ar/net/aspose.words/nodeimporter/nodeimporter/
---
## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode) {#constructor}

يقوم بتهيئة مثيل جديد لملف[`NodeImporter`](../../nodeimporter) فئة ._ x000d_

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | DocumentBase | وثيقة المصدر. |
| dstDoc | DocumentBase | المستند الوجهة الذي سيكون مالك العقد المستوردة. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيق النمط الذي يتعارض. |

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

* class [DocumentBase](../../documentbase)
* enum [ImportFormatMode](../../importformatmode)
* class [NodeImporter](../../nodeimporter)
* مساحة الاسم [Aspose.Words](../../nodeimporter)
* المجسم [Aspose.Words](../../../)

---

## NodeImporter(DocumentBase, DocumentBase, ImportFormatMode, ImportFormatOptions) {#constructor_1}

يقوم بتهيئة مثيل جديد لملف[`NodeImporter`](../../nodeimporter) فئة ._ x000d_

```csharp
public NodeImporter(DocumentBase srcDoc, DocumentBase dstDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| srcDoc | DocumentBase | وثيقة المصدر. |
| dstDoc | DocumentBase | المستند الوجهة الذي سيكون مالك العقد المستوردة. |
| importFormatMode | ImportFormatMode | يحدد كيفية دمج تنسيق النمط الذي يتعارض. |
| importFormatOptions | ImportFormatOptions | يحدد خيارات متنوعة لتنسيق العقدة المستوردة. |

### أمثلة

يعرض كيفية حل التعارض عند استيراد المستندات التي تحتوي على قوائم بنفس معرف تعريف القائمة.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// اضبط خاصية "KeepSourceNumbering" على "true" لتطبيق معرف تعريف قائمة مختلف
// إلى أنماط متطابقة مثل Aspose.Words تستوردها إلى مستندات الوجهة.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

يوضح كيفية حل تعارضات ترقيم القائمة في مستندات المصدر والوجهة.

```csharp
// افتح مستندًا بنظام ترقيم قائمة مخصص ، ثم انسخه.
// نظرًا لأن كلاهما لهما نفس تنسيق الترقيم ، فستتعارض التنسيقات إذا قمنا باستيراد مستند إلى الآخر.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// عندما نستورد نسخة المستند إلى النسخة الأصلية ثم نلحقها ،
// ثم ستنضم القائمتان بنفس تنسيق القائمة.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" على "خطأ" ، فسيتم استنساخ القائمة من المستند
// التي نلحقها بالأصل ستستمر في ترقيم القائمة التي نلحقها بها.
// سيؤدي هذا إلى دمج القائمتين في قائمة واحدة.
// إذا قمنا بتعيين علامة "KeepSourceNumbering" على "true" ، فسيتم استنساخ المستند
// ستحتفظ القائمة بترقيمها الأصلي ، مما يجعل القائمتين تظهران كقائمتين منفصلتين. 
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

* class [DocumentBase](../../documentbase)
* enum [ImportFormatMode](../../importformatmode)
* class [ImportFormatOptions](../../importformatoptions)
* class [NodeImporter](../../nodeimporter)
* مساحة الاسم [Aspose.Words](../../nodeimporter)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
