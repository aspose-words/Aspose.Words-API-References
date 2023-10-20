---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words لـ .NET
description: Aspose.Words.NodeImporter فصل. يسمح بإجراء الاستيراد المتكرر للعقد من مستند إلى آخر بكفاءة في C#.
type: docs
weight: 4210
url: /ar/net/aspose.words/nodeimporter/
---
## NodeImporter class

يسمح بإجراء الاستيراد المتكرر للعقد من مستند إلى آخر بكفاءة.

لمعرفة المزيد، قم بزيارة[نموذج كائن مستند Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class NodeImporter
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | تهيئة مثيل جديد لـ`NodeImporter` فئة. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | تهيئة مثيل جديد لـ`NodeImporter` فئة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | يستورد عقدة من مستند إلى آخر. |

## ملاحظات

يوفر Aspose.Words وظيفة لسهولة نسخ ونقل fragments بين مستندات Microsoft Word. يُعرف هذا باسم "استيراد العقد". قبل أن تتمكن من إدراج جزء من مستند إلى آخر، تحتاج إلى "استيراده". يؤدي الاستيراد إلى إنشاء نسخة عميقة من العقدة الأصلية، جاهزة للإدراج في مستند الوجهة .

إن أبسط طريقة لاستيراد عقدة هي استخدام[`ImportNode`](../documentbase/importnode/) method المقدمة من[`DocumentBase`](../documentbase/) هدف.

ومع ذلك، عندما تحتاج إلى استيراد العقد من مستند إلى آخر عدة مرات، فمن الأفضل استخدام`NodeImporter` فصل. ال`NodeImporter` تسمح فئة بتقليل عدد الأنماط والقوائم التي تم إنشاؤها في المستند الوجهة.

يمثل نسخ أو نقل الأجزاء من مستند Microsoft Word إلى مستند آخر عددًا من التحديات التقنية لـ Aspose.Words. في مستند Word، يتم تخزين الأنماط وتنسيق القائمة مركزيًا، بشكل منفصل عن نص المستند. تشير الفقرات وعمليات النص فقط إلى الأنماط بواسطة معرفات فريدة داخلية.

تنشأ التحديات من حقيقة اختلاف الأنماط والقوائم في المستندات المختلفة. على سبيل المثال، لنسخ فقرة منسقة بنمط العنوان 1 من مستند إلى آخر، يجب أخذ عدد من الأشياء في الاعتبار: تحديد ما إذا كنت تريد ذلك أم لا انسخ نمط العنوان 1 من المستند المصدر إلى المستند الوجهة، واستنسخ الفقرة، وقم بتحديث الفقرة المستنسخة بحيث تشير إلى نمط العنوان 1 الصحيح في المستند الوجهة. إذا كان لا بد من نسخ النمط، فسيتم نسخ جميع الأنماط التي يتضمنها يجب تحليل المراجع (المعتمدة على style ونمط الفقرة التالية) وربما نسخها أيضًا وما إلى ذلك. توجد مشكلات مماثلة عند نسخ فقرات ذات تعداد نقطي أو رقمي لأن Microsoft Word يخزن تعريفات القائمة بشكل منفصل عن النص.

ال`NodeImporter`تشبه الفئة السياق الذي يحتوي على "جداول الترجمة" أثناء الاستيراد. إنه يترجم بشكل صحيح بين الأنماط والقوائم في المستندات المصدر و الوجهة.

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
