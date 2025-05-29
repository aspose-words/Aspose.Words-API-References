---
title: Range.Replace
linktitle: Replace
articleTitle: Replace
second_title: Aspose.Words لـ .NET
description: استبدل جميع أنماط سلسلة الأحرف بسهولة باستخدام طريقة استبدال النطاق. حسّن معالجة النصوص لديك بهذه الأداة الفعّالة!
type: docs
weight: 100
url: /ar/net/aspose.words/range/replace/
---
## Replace(*string, string*) {#replace}

يستبدل جميع حالات نمط سلسلة الأحرف المحددة بسلسلة بديلة.

```csharp
public int Replace(string pattern, string replacement)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

لن يتم استخدام النمط كتعبير عادي. يرجى الاستخدام`Replace` إذا كنت بحاجة إلى تعبيرات منتظمة.

تم استخدام المقارنة غير الحساسة لحالة الأحرف.

تتمكن الطريقة من معالجة الانقطاعات في كل من النمط والسلاسل البديلة.

يجب عليك استخدام أحرف خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **&amp;ص** - فاصل الفقرة
* **&amp;ب** - فاصل القسم
* **&amp;م** - كسر الصفحة
* **&amp;ل** - كسر السطر يدويًا

طريقة الاستخدام`Replace` للحصول على تخصيص أكثر مرونة.

## أمثلة

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// إدراج فاصل الفقرة بعد الأرقام.
doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
```

يوضح كيفية إجراء عملية البحث عن نص واستبداله في محتويات المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Greetings, _FullName_!");

// قم بإجراء عملية بحث واستبدال على محتويات مستندنا وتحقق من عدد عمليات الاستبدال التي تمت.
int replacementCount = doc.Range.Replace("_FullName_", "John Doe");

Assert.AreEqual(1, replacementCount);
Assert.AreEqual("Greetings, John Doe!", doc.GetText().Trim());
```

يوضح كيفية إضافة التنسيق إلى الفقرات التي عثرت فيها عملية البحث والاستبدال على تطابقات.

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

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط خاصية "المحاذاة" على "ParagraphAlignment.Right" لمحاذاة كل فقرة إلى اليمين
// الذي يحتوي على تطابق وجدته عملية البحث والاستبدال.
options.ApplyParagraphFormat.Alignment = ParagraphAlignment.Right;

// استبدل كل نقطة تقع قبل فاصل الفقرة بعلامة تعجب.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*Regex, string*) {#replace_2}

يستبدل جميع حالات نمط الأحرف المحدد بواسطة تعبير عادي بسلسلة أخرى.

```csharp
public int Replace(Regex pattern, string replacement)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

يستبدل المطابقة بأكملها التي تم التقاطها بواسطة التعبير العادي.

تتمكن الطريقة من معالجة الانقطاعات في كل من النمط والسلاسل البديلة.

يجب عليك استخدام أحرف خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **&amp;ص** - فاصل الفقرة
* **&amp;ب** - فاصل القسم
* **&amp;م** - كسر الصفحة
* **&amp;ل** - كسر السطر يدويًا

طريقة الاستخدام`Replace` للحصول على تخصيص أكثر مرونة.

## أمثلة

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

//استبدال كل رقم بفاصل الفقرة.
doc.Range.Replace(new Regex(@"\d+"), "&p");
```

يوضح كيفية استبدال كافة حالات نمط التعبير العادي بنص آخر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("I decided to get the curtains in gray, ideal for the grey-accented room.");

doc.Range.Replace(new Regex("gr(a|e)y"), "lavender");

Assert.AreEqual("I decided to get the curtains in lavender, ideal for the lavender-accented room.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_1}

يستبدل جميع حالات نمط سلسلة الأحرف المحددة بسلسلة بديلة.

```csharp
public int Replace(string pattern, string replacement, FindReplaceOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pattern | String | سلسلة ليتم استبدالها. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

لن يتم استخدام النمط كتعبير عادي. يرجى الاستخدام`Replace` إذا كنت بحاجة إلى تعبيرات منتظمة.

تتمكن الطريقة من معالجة الانقطاعات في كل من النمط والسلاسل البديلة.

يجب عليك استخدام أحرف خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **&amp;ص** - فاصل الفقرة
* **&amp;ب** - فاصل القسم
* **&amp;م** - كسر الصفحة
* **&amp;ل** - كسر السطر يدويًا
* **&amp;&amp;** - &amp; شخصية

## أمثلة

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Numbers 1, 2, 3");

// إدراج فاصل الفقرة بعد الأرقام.
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

يوضح كيفية تبديل حساسية الحالة عند إجراء عملية البحث والاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "MatchCase" على "true" لتطبيق حساسية الحالة أثناء البحث عن السلاسل التي يجب استبدالها.
// اضبط علامة "MatchCase" على "false" لتجاهل حالة الأحرف أثناء البحث عن نص لاستبداله.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

يوضح كيفية تبديل عمليات البحث والاستبدال الخاصة بالكلمات المستقلة فقط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
FindReplaceOptions options = new FindReplaceOptions();

// اضبط علامة "FindWholeWordsOnly" على "true" لاستبدال النص الموجود إذا لم يكن جزءًا من كلمة أخرى.
// اضبط علامة "FindWholeWordsOnly" على "false" لاستبدال كل النص بغض النظر عن محيطه.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

يوضح كيفية استبدال كافة مثيلات سلسلة النص في جدول وخلية.

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

// تنفيذ عملية البحث والاستبدال على جدول بأكمله.
table.Range.Replace("Carrots", "Eggs", options);

// قم بإجراء عملية البحث والاستبدال على الخلية الأخيرة من الصف الأخير من الجدول.
table.LastRow.LastCell.Range.Replace("50", "20", options);

Assert.AreEqual("Eggs\a50\a\a" +
                "Potatoes\a20\a\a", table.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## Replace(*Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replace_3}

يستبدل جميع حالات نمط الأحرف المحدد بواسطة تعبير عادي بسلسلة أخرى.

```csharp
public int Replace(Regex pattern, string replacement, FindReplaceOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pattern | Regex | نمط تعبير منتظم يستخدم للعثور على المطابقات. |
| replacement | String | سلسلة لاستبدال كافة حالات النمط. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) كائن لتحديد خيارات إضافية. |

### قيمة الإرجاع

عدد الاستبدالات التي تم إجراؤها.

## ملاحظات

يستبدل المطابقة بأكملها التي تم التقاطها بواسطة التعبير العادي.

تتمكن الطريقة من معالجة الانقطاعات في كل من النمط والسلاسل البديلة.

يجب عليك استخدام أحرف خاصة إذا كنت بحاجة إلى العمل مع الفواصل:

* **&amp;ص** - فاصل الفقرة
* **&amp;ب** - فاصل القسم
* **&amp;م** - كسر الصفحة
* **&amp;ل** - كسر السطر يدويًا
* **&amp;&amp;** - &amp; شخصية

## أمثلة

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("a1, b2, c3");

//استبدال كل رقم بفاصل الفقرة.
doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
```

يوضح كيفية استبدال جميع حالات نمط التعبير العادي بسلسلة أخرى، مع تتبع كل هذه الاستبدالات.

```csharp
public void ReplaceWithCallback()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Our new location in New York City is opening tomorrow. " +
                    "Hope to see all our NYC-based customers at the opening!");

    // يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
    FindReplaceOptions options = new FindReplaceOptions();

    // قم بتعيين معاودة الاتصال لتتبع أي عمليات استبدال ستقوم بها طريقة "الاستبدال".
    TextFindAndReplacementLogger logger = new TextFindAndReplacementLogger();
    options.ReplacingCallback = logger;

    doc.Range.Replace(new Regex("New York City|NYC"), "Washington", options);

    Assert.AreEqual("Our new location in (Old value:\"New York City\") Washington is opening tomorrow. " +
                    "Hope to see all our (Old value:\"NYC\") Washington-based customers at the opening!", doc.GetText().Trim());

    Assert.AreEqual("\"New York City\" converted to \"Washington\" 20 characters into a Run node.\r\n" +
                    "\"NYC\" converted to \"Washington\" 42 characters into a Run node.", logger.GetLog().Trim());
}

/// <summary>
/// يحتفظ بسجل لكل استبدال نص تم إجراؤه بواسطة عملية البحث والاستبدال
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

يوضح كيفية إدراج محتويات مستند بأكمله كبديل لمطابقة في عملية البحث والاستبدال.

```csharp
public void InsertDocumentAtReplace()
{
    Document mainDoc = new Document(MyDir + "Document insertion destination.docx");

    // يمكننا استخدام الكائن "FindReplaceOptions" لتعديل عملية البحث والاستبدال.
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

        //أدرج مستندًا بعد الفقرة التي تحتوي على النص المطابق.
        Paragraph para = (Paragraph)args.MatchNode.ParentNode;
        InsertDocument(para, subDoc);

        // قم بإزالة الفقرة التي تحتوي على النص المطابق.
        para.Remove();

        return ReplaceAction.Skip;
    }
}

/// <summary>
/// إدراج جميع عقد مستند آخر بعد فقرة أو جدول.
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
                // تخطي العقدة إذا كانت الفقرة الفارغة الأخيرة في القسم.
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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
