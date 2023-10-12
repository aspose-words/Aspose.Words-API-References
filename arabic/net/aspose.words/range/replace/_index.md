---
title: Range.Replace
second_title: Aspose.Words لمراجع .NET API
description: Range طريقة. يستبدل كافة تكرارات نمط سلسلة الأحرف المحددة بسلسلة بديلة.
type: docs
weight: 90
url: /ar/net/aspose.words/range/replace/
---
## Replace(string, string) {#replace}

يستبدل كافة تكرارات نمط سلسلة الأحرف المحددة بسلسلة بديلة.

```csharp
public int Replace(string pattern, string replacement)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة تكرارات النمط. |

### قيمة الإرجاع

عدد البدائل التي تم إجراؤها.

### ملاحظات

لن يتم استخدام النمط كتعبير عادي. يرجى استخدامه`Replace`إذا كنت بحاجة إلى تعبيرات عادية.

تستخدم مقارنة غير حساسة لحالة الأحرف.

الطريقة قادرة على معالجة الفواصل في كل من سلاسل النمط والاستبدال.

يجب عليك استخدام أحرف وصفية خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **&amp; ص** - فاصل الفقرة
* **&amp;ب** - فاصل المقطع
* **&amp; م** - فاصل صفحة
* **&amp; ل** - فاصل الأسطر اليدوي

طريقة الاستخدام`Replace` للحصول على تخصيص أكثر مرونة.

### أمثلة

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// إدراج فاصل فقرة بعد الأرقام.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

يوضح كيفية إجراء عملية البحث عن النص واستبداله على محتويات المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// إجراء عملية بحث واستبدال على محتويات وثيقتنا والتحقق من عدد عمليات الاستبدال التي تمت.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

يوضح كيفية إضافة تنسيق إلى الفقرات التي عثرت فيها عملية البحث والاستبدال على تطابقات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Every paragraph that ends with a full stop like this one will be right aligned.");
builder.Writeln("This one will not!");
builder.Write("This one also will.");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(ParagraphAlignment.Left, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[2].ParagraphFormat.Alignment);

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط خاصية "المحاذاة" على "ParagraphAlignment.Right" لمحاذاة كل فقرة إلى اليمين
// يحتوي على التطابق الذي وجدته عملية البحث والاستبدال.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// استبدل كل نقطة قبل فاصل الفقرة بعلامة تعجب.
int count = doc.Range.Replace(".&p", "!&p", options);

Assert.AreEqual(2, count);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[2].ParagraphFormat.Alignment);
Assert.AreEqual("Every paragraph that ends with a full stop like this one will be right aligned!\r" +
                "This one will not!\r" +
                "This one also will!", doc.GetText().Trim());
```

### أنظر أيضا

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../range/)
* المجسم [Aspose.Words](../../../)

---

## Replace(Regex, string) {#replace_2}

يستبدل كافة تكرارات نمط الأحرف المحدد بواسطة تعبير عادي بسلسلة أخرى.

```csharp
public int Replace(Regex pattern, string replacement)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pattern | Regex | نمط تعبير عادي يستخدم للعثور على التطابقات. |
| replacement | String | سلسلة لاستبدال كافة تكرارات النمط. |

### قيمة الإرجاع

عدد البدائل التي تم إجراؤها.

### ملاحظات

يستبدل المطابقة بأكملها التي تم التقاطها بواسطة التعبير العادي.

الطريقة قادرة على معالجة الفواصل في كل من سلاسل النمط والاستبدال.

يجب عليك استخدام أحرف وصفية خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **&amp; ص** - فاصل الفقرة
* **&amp;ب** - فاصل المقطع
* **&amp; م** - فاصل صفحة
* **&amp; ل** - فاصل الأسطر اليدوي

طريقة الاستخدام`Replace` للحصول على تخصيص أكثر مرونة.

### أمثلة

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// يستبدل كل رقم بفاصل الفقرة.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

يوضح كيفية استبدال كافة تكرارات نمط التعبير العادي بنص آخر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../range/)
* المجسم [Aspose.Words](../../../)

---

## Replace(string, string, FindReplaceOptions) {#replace_1}

يستبدل كافة تكرارات نمط سلسلة الأحرف المحددة بسلسلة بديلة.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة تكرارات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد البدائل التي تم إجراؤها.

### ملاحظات

لن يتم استخدام النمط كتعبير عادي. يرجى استخدامه`Replace`إذا كنت بحاجة إلى تعبيرات عادية.

الطريقة قادرة على معالجة الفواصل في كل من سلاسل النمط والاستبدال.

يجب عليك استخدام أحرف وصفية خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **&amp; ص** - فاصل الفقرة
* **&amp;ب** - فاصل المقطع
* **&amp; م** - فاصل صفحة
* **&amp; ل** - فاصل الأسطر اليدوي
* **&amp;&amp;** - &amp; شخصية

### أمثلة

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// إدراج فاصل فقرة بعد الأرقام.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

يوضح كيفية استبدال النص في تذييل المستند.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

يوضح كيفية تبديل حساسية حالة الأحرف عند إجراء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "MatchCase" على "صحيح" لتطبيق حساسية حالة الأحرف أثناء البحث عن سلاسل لاستبدالها.
// اضبط علامة "MatchCase" على "خطأ" لتجاهل حالة الأحرف أثناء البحث عن نص لاستبداله.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

يوضح كيفية تبديل عمليات البحث والاستبدال المستقلة للكلمات فقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "FindWholeWordsOnly" على "صحيح" لاستبدال النص الذي تم العثور عليه إذا لم يكن جزءًا من كلمة أخرى.
// اضبط علامة "FindWholeWordsOnly" على "خطأ" لاستبدال النص بالكامل بغض النظر عن البيئة المحيطة به.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

يوضح كيفية استبدال كافة مثيلات سلسلة النص في الجدول والخلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Carrots");
builder.InsertCell();
builder.Write("50");
builder.EndRow();
builder.InsertCell();
builder.Write("Potatoes");
builder.InsertCell();
builder.Write("50");
builder.EndTable();

FindReplaceOptions options = new FindReplaceOptions();
options.MatchCase = true;
options.FindWholeWordsOnly = true;

// إجراء عملية البحث والاستبدال على الجدول بأكمله.
table.Range.Replace("Carrots", "Eggs", options);

// إجراء عملية البحث والاستبدال في الخلية الأخيرة من الصف الأخير من الجدول.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* مساحة الاسم [Aspose.Words](../../range/)
* المجسم [Aspose.Words](../../../)

---

## Replace(Regex, string, FindReplaceOptions) {#replace_3}

يستبدل كافة تكرارات نمط الأحرف المحدد بواسطة تعبير عادي بسلسلة أخرى.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pattern | Regex | نمط تعبير عادي يستخدم للعثور على التطابقات. |
| replacement | String | سلسلة لاستبدال كافة تكرارات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد البدائل التي تم إجراؤها.

### ملاحظات

يستبدل المطابقة بأكملها التي تم التقاطها بواسطة التعبير العادي.

الطريقة قادرة على معالجة الفواصل في كل من سلاسل النمط والاستبدال.

يجب عليك استخدام أحرف وصفية خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **&amp; ص** - فاصل الفقرة
* **&amp;ب** - فاصل المقطع
* **&amp; م** - فاصل صفحة
* **&amp; ل** - فاصل الأسطر اليدوي
* **&amp;&amp;** - &amp; شخصية

### أمثلة

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

// يستبدل كل رقم بفاصل الفقرة.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

يوضح كيفية استبدال كافة تكرارات نمط التعبير العادي بسلسلة أخرى، مع تتبع كل هذه الاستبدالات.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // قم بتعيين رد اتصال يتتبع أي بدائل ستجريها طريقة "الاستبدال".
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
/// ويلاحظ قيمة النص المطابق الأصلي.
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

يوضح كيفية إدراج محتويات المستند بالكامل كبديل لمطابقة في عملية البحث والاستبدال.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // يمكننا استخدام كائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();
    options.ReplacingCallback = new InsertDocumentAtReplaceHandler();

    mainDoc.Range.Replace(new Regex("\\[MY_DOCUMENT\\]"), "", options);
    mainDoc.Save(ArtifactsDir + "InsertDocument.InsertDocumentAtReplace.docx");

}

private class InsertDocumentAtReplaceHandler : IReplacingCallback
{
    ReplaceAction IReplacingCallback.Replacing(ReplacingArgs args)
    {
        Document subDoc = new Document(MyDir + "Document.docx");

        // أدخل مستندًا بعد الفقرة التي تحتوي على النص المطابق.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // قم بإزالة الفقرة التي تحتوي على النص المطابق.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// إدراج كافة العقد في مستند آخر بعد فقرة أو جدول.
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

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* مساحة الاسم [Aspose.Words](../../range/)
* المجسم [Aspose.Words](../../../)


