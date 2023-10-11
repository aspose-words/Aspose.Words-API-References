---
title: DocumentBuilder.InsertHtml
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج سلسلة HTML في المستند.
type: docs
weight: 360
url: /ar/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(string) {#inserthtml}

إدراج سلسلة HTML في المستند.

```csharp
public void InsertHtml(string html)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| html | String | سلسلة HTML لإدراجها في المستند. |

### ملاحظات

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML بأكمله.

### أمثلة

يوضح كيفية استخدام منشئ المستندات لإدراج محتوى html في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// يؤدي إدخال كود HTML إلى تحليل تنسيق كل عنصر إلى تنسيق نص مستند مكافئ.
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual("Paragraph right", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

Assert.AreEqual("Implicit paragraph left", paragraphs[1].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Left, paragraphs[1].ParagraphFormat.Alignment);
Assert.True(paragraphs[1].Runs[0].Font.Bold);

Assert.AreEqual("Div center", paragraphs[2].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Center, paragraphs[2].ParagraphFormat.Alignment);

Assert.AreEqual("Heading 1 left.", paragraphs[3].GetText().Trim());
Assert.AreEqual("Heading 1", paragraphs[3].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtml.docx");
```

يوضح كيفية تنفيذ عملية دمج البريد باستخدام رد اتصال مخصص يتعامل مع بيانات الدمج في شكل مستندات HTML.

```csharp
public void MergeHtml()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(@"MERGEFIELD  html_Title  \b Content");
    builder.InsertField(@"MERGEFIELD  html_Body  \b Content");

    object[] mergeData =
    {
        "<html>" +
            "<h1>" +
                "<span style=\"color: #0000ff; font-family: Arial;\">Hello World!</span>" +
            "</h1>" +
        "</html>", 

        "<html>" +
            "<blockquote>" +
                "<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>" +
            "</blockquote>" +
        "</html>"
    };

    doc.MailMerge.FieldMergingCallback = new HandleMergeFieldInsertHtml();
    doc.MailMerge.Execute(new[] { "html_Title", "html_Body" }, mergeData);

    doc.Save(ArtifactsDir + "MailMergeEvent.MergeHtml.docx");
}

/// <summary>
/// إذا واجه دمج البريد MERGEFIELD الذي يبدأ اسمه بالبادئة "html_"،
/// يقوم رد الاتصال هذا بتحليل بيانات الدمج الخاصة به كمحتوى HTML وإضافة النتيجة إلى موقع مستند MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// يتم الاتصال به عندما يقوم دمج البريد بدمج البيانات في MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // أضف بيانات HTML التي تم تحليلها إلى نص المستند.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // نظرًا لأننا قمنا بالفعل بإدراج المحتوى المدمج يدويًا،
             // لن نحتاج إلى الرد على هذا الحدث من خلال إعادة المحتوى عبر خاصية "النص".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        // لا تفعل شيئا.
    }
}
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertHtml(string, bool) {#inserthtml_2}

إدراج سلسلة HTML في المستند.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| html | String | سلسلة HTML لإدراجها في المستند. |
| useBuilderFormatting | Boolean | قيمة تشير إلى ما إذا كان التنسيق محددًا أم لا[`DocumentBuilder`](../) يتم استخدام كتنسيق أساسي للنص المستورد من HTML. |

### ملاحظات

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML بأكمله.

متى*useBuilderFormatting* يكون`خطأ شنيع`[`DocumentBuilder`](../)يتم تجاهل التنسيق ويعتمد تنسيق text المدرج على تنسيق HTML الافتراضي. ونتيجة لذلك، يبدو النص كما هو معروض في المتصفحات.

متى*useBuilderFormatting* يكون`حقيقي` ، يعتمد تنسيق النص المدرج[`DocumentBuilder`](../) التنسيق، ويبدو النص كما لو تم إدراجه به[`Write`](../write/) .

### أمثلة

يوضح كيفية تطبيق تنسيق أداة إنشاء المستندات أثناء إدراج محتوى HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين محاذاة النص للمنشئ، وأدخل فقرة HTML بمحاذاة محددة وأخرى بدونها.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// تحتوي الفقرة الأولى على محاذاة محددة. عندما يقوم InsertHtml بتحليل تعليمات HTML البرمجية،
// قيمة محاذاة الفقرة الموجودة في كود HTML تحل دائمًا محل قيمة منشئ المستندات.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// لم يتم تحديد محاذاة للفقرة الثانية. يمكن ملء قيمة المحاذاة الخاصة بها
// حسب قيمة المنشئ اعتمادًا على العلامة التي مررناها إلى طريقة InsertHtml.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)

---

## InsertHtml(string, HtmlInsertOptions) {#inserthtml_1}

يقوم بإدراج سلسلة HTML في المستند. يسمح بتحديد خيارات إضافية.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| html | String | سلسلة HTML لإدراجها في المستند. |
| options | HtmlInsertOptions | الخيارات التي يتم استخدامها عند إدراج سلسلة HTML. |

### ملاحظات

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML بأكمله.

### أمثلة

يوضح كيفية استخدام الخيارات أثناء إدراج HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// افتراضيًا، يقوم "DocumentBuilder.InsertHtml" بإدراج جزء HTML ينتهي بعنصر HTML على مستوى الكتلة،
// يقوم عادةً بإغلاق عنصر مستوى الكتلة وإدراج فاصل فقرة.
// نتيجة لذلك، تظهر فقرة فارغة جديدة بعد إدراج المستند.
// إذا قمنا بتحديد "HtmlInsertOptions.RemoveLastEmptyParagraph"، فستتم إزالة تلك الفقرات الفارغة الإضافية.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### أنظر أيضا

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


