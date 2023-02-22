---
title: Enum ReplaceAction
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Replacing.ReplaceAction تعداد. يسمح للمستخدم بتحديد ما يحدث للمطابقة الحالية أثناء عملية الاستبدال.
type: docs
weight: 4380
url: /ar/net/aspose.words.replacing/replaceaction/
---
## ReplaceAction enumeration

يسمح للمستخدم بتحديد ما يحدث للمطابقة الحالية أثناء عملية الاستبدال.

```csharp
public enum ReplaceAction
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Replace | `0` | استبدال المطابقة الحالية . |
| Skip | `1` | تخطي المباراة الحالية . |
| Stop | `2` | قم بإنهاء عملية الاستبدال. |

### أمثلة

يوضح كيفية إدراج محتويات المستند بالكامل كبديل لمطابقة في عملية البحث والاستبدال.

```csharp
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // أدخل مستندًا بعد الفقرة التي تحتوي على النص المطابق.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // إزالة الفقرة مع النص المتطابق.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// يُدرج كل عقد مستند آخر بعد فقرة أو جدول.
/// </summary>
private static void InsertDocument(Node insertionDestination, Document docToInsert)
{
    if (insertionDestination.NodeType == NodeType.Paragraph || insertionDestination.NodeType == NodeType.Table)
    {
        CompositeNode dstStory = insertionDestination.ParentNode;

        NodeImporter importer =
            new NodeImporter(docToInsert, insertionDestination.Document, ImportFormatMode.KeepSourceFormatting);

        foreach (Section srcSection in docToInsert.Sections.OfType<Section>())
            foreach (Node srcNode in srcSection.Body)
            {
                // تخطي العقدة إذا كانت آخر فقرة فارغة في القسم.
                if (srcNode.NodeType == NodeType.Paragraph)
                {
                    Paragraph para = (Paragraph)srcNode;
                    if (para.IsEndOfSection && !para.HasChildNodes)
                        continue;
                }

                Node newNode = importer.ImportNode(srcNode, true);

                dstStory.InsertAfter(newNode, insertionDestination);
                insertionDestination = newNode;
            }
    }
    else
    {
        throw new ArgumentException("The destination node must be either a paragraph or table.");
    }
}
```

### أنظر أيضا

* interface [IReplacingCallback](../ireplacingcallback/)
* class [Range](../../aspose.words/range/)
* method [Replace](../../aspose.words/range/replace/)
* مساحة الاسم [Aspose.Words.Replacing](../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../)


