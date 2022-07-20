---
title: IReplacingCallback
second_title: Aspose.Words لمراجع .NET API
description: قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طريقتك المخصصة أثناء عملية البحث والاستبدال.
type: docs
weight: 4370
url: /ar/net/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface

قم بتنفيذ هذه الواجهة إذا كنت تريد استدعاء طريقتك المخصصة أثناء عملية البحث والاستبدال.

```csharp
public interface IReplacingCallback
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Replacing](../../aspose.words.replacing/ireplacingcallback/replacing)(ReplacingArgs) | طريقة يحددها المستخدم يتم استدعاؤها أثناء عملية الاستبدال لكل تطابق يتم العثور عليه قبل إجراء الاستبدال. |

### أمثلة

يوضح كيفية استبدال كل تكرارات نمط التعبير العادي بسلسلة أخرى ، أثناء تتبع كل هذه الاستبدالات.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // تعيين رد اتصال يتتبع أي بدائل تقوم بها طريقة "استبدال".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// يحتفظ بسجل لكل استبدال نص يتم إجراؤه بواسطة عملية البحث والاستبدال
/// ويلاحظ قيمة النص المتطابق الأصلي.
/// </summary>
private class TextFindAndReplacementLogger : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        mLog.AppendLine($"\"{args.Match.Value}\" converted to \"{args.Replacement}\" " +
                        $"{args.MatchOffset} characters into a {args.MatchNode.NodeType} node.");

        args.Replacement = $"(Old value:\"{args.Match.Value}\") {args.Replacement}";
        return ReplaceAction.Replace;
    }

    public string GetLog()
    {
        return mLog.ToString();
    }

    private readonly StringBuilder mLog = new StringBuilder();
}
```

يوضح كيفية تعقب الترتيب الذي تتجاوز به عملية استبدال النص العقد.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
        {
            Document doc = new Document(MyDir + "Header and footer types.docx");

            Section firstPageSection = doc.FirstSection;

            ReplaceLog logger = new ReplaceLog();
            FindReplaceOptions options = new FindReplaceOptions { ReplacingCallback = logger };

            // سيؤثر استخدام رأس / تذييل مختلف للصفحة الأولى على ترتيب البحث.
            firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
            doc.Range.Replace(new Regex("(header|footer)"), "", options);

#if NET48 || NET5_0_OR_GREATER || JAVA
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
                    logger.Text.Replace("\r", ""));
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
                    logger.Text.Replace("\r", ""));
#elif __MOBILE__
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", logger.Text);
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", logger.Text);
#endif
        }

        /// <summary>
        /// أثناء عملية البحث والاستبدال ، يسجل محتويات كل عقدة تحتوي على نص "تعثر عليه" العملية ،
        /// في الحالة التي كانت عليها قبل حدوث الاستبدال.
        /// سيعرض هذا الترتيب الذي تتجاوز به عملية استبدال النص العقد.
        /// </summary>
        private class ReplaceLog : IReplacingCallback
        {
            public ReplaceAction Replacing(ReplacingArgs args)
            {
                mTextBuilder.AppendLine(args.MatchNode.GetText());
                return ReplaceAction.Skip;
            }

            internal string Text => mTextBuilder.ToString();

            private readonly StringBuilder mTextBuilder = new StringBuilder();
        }
```

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

* مساحة الاسم [Aspose.Words.Replacing](../../aspose.words.replacing)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
