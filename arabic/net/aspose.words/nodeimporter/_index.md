---
title: NodeImporter Class
linktitle: NodeImporter
articleTitle: NodeImporter
second_title: Aspose.Words لـ .NET
description: انقل عُقد المستندات بسهولة مع Aspose.Words.NodeImporter. بسّط سير عملك وحسّن كفاءة إدارة مستنداتك اليوم!
type: docs
weight: 4900
url: /ar/net/aspose.words/nodeimporter/
---
## NodeImporter class

يسمح بإجراء استيراد متكرر للعقد من مستند إلى آخر بكفاءة.

لمعرفة المزيد، قم بزيارة[نموذج كائن المستند (DOM) في Aspose.Words](https://docs.aspose.com/words/net/aspose-words-document-object-model/) مقالة توثيقية.

```csharp
public class NodeImporter
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [NodeImporter](nodeimporter/#constructor)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/)*) | يقوم بتهيئة مثيل جديد لـ`NodeImporter` الصف. |
| [NodeImporter](nodeimporter/#constructor_1)(*[DocumentBase](../documentbase/), [DocumentBase](../documentbase/), [ImportFormatMode](../importformatmode/), [ImportFormatOptions](../importformatoptions/)*) | يقوم بتهيئة مثيل جديد لـ`NodeImporter` الصف. |

## طُرق

| اسم | وصف |
| --- | --- |
| [ImportNode](../../aspose.words/nodeimporter/importnode/)(*[Node](../node/), bool*) | استيراد عقدة من مستند إلى آخر. |

## ملاحظات

يوفر Aspose.Words وظيفةً تُسهّل نسخ ونقل شظايا بين مستندات مايكروسوفت وورد. تُعرف هذه العملية باسم "استيراد العقد". قبل إدراج شظية من مستند إلى آخر، يجب عليك "استيرادها". يُنشئ الاستيراد نسخةً كاملةً من العقدة الأصلية، جاهزةً للإدراج في مستند الوجهة .

أبسط طريقة لاستيراد عقدة هي استخدام[`ImportNode`](../documentbase/importnode/) الطريقة المقدمة بواسطة[`DocumentBase`](../documentbase/) هدف.

ومع ذلك، عندما تحتاج إلى استيراد العقد من مستند إلى آخر عدة مرات، فمن الأفضل استخدام الأمر x000d_`NodeImporter` الصف. ال`NodeImporter` تسمح فئة بتقليل عدد الأنماط والقوائم التي تم إنشاؤها في المستند الوجهة.

يُمثل نسخ أو نقل أجزاء من مستند مايكروسوفت وورد إلى آخر عددًا كبيرًا من التحديات التقنية لـ Aspose.Words. في مستند وورد، تُخزَّن الأنماط وتنسيقات القوائم مركزيًا، بشكل منفصل عن نص المستند. تُشير الفقرات وسلاسل النصوص إلى الأنماط فقط من خلال مُعرِّفات فريدة داخلية.

تنشأ التحديات من حقيقة أن الأنماط والقوائم تختلف في المستندات المختلفة. على سبيل المثال، لنسخ فقرة منسقة بنمط العنوان 1 من مستند إلى آخر، يجب أخذ عدد من الأشياء في الاعتبار: تحديد ما إذا كان سيتم نسخ نمط العنوان 1 من المستند المصدر إلى المستند الوجهة، واستنساخ الفقرة، وتحديث الفقرة المستنسخة بحيث تشير إلى نمط العنوان 1 الصحيح في المستند الوجهة. إذا كان يجب نسخ النمط، فيجب تحليل جميع الأنماط التي يشير إليها (بناءً على style ونمط الفقرة التالية) وربما نسخها أيضًا وما إلى ذلك. توجد مشكلات مماثلة عند نسخ الفقرات المنقطة أو المرقمة لأن Microsoft Word يخزن تعريفات القائمة بشكل منفصل عن النص.

ال`NodeImporter`الفئة أشبه بالسياق، إذ تحتفظ بـ "جداول الترجمة" أثناء الاستيراد. وهي تترجم بشكل صحيح بين الأنماط والقوائم في مستندي المصدر و الوجهة.

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
