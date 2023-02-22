---
title: DocumentBuilder.InsertHtml
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج سلسلة HTML في المستند.
type: docs
weight: 330
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

يوضح كيفية استخدام منشئ المستندات لإدراج محتوى html في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// إدراج كود HTML يوزع تنسيق كل عنصر في تنسيق نص الوثيقة المكافئ.
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

يوضح كيفية تنفيذ دمج المراسلات باستخدام رد اتصال مخصص يعالج بيانات الدمج في شكل مستندات HTML.

```csharp
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
/// إذا واجه دمج البريد MERGEFIELD يبدأ اسمه بالبادئة "html_" ،
/// هذا الاستدعاء يحلل بيانات الدمج الخاصة به كمحتوى HTML ويضيف النتيجة إلى موقع المستند الخاص بـ MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// يتم الاستدعاء عندما يقوم دمج المراسلات بدمج البيانات في MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // أضف بيانات HTML التي تم تحليلها إلى نص المستند.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // نظرًا لأننا أدخلنا المحتوى المدمج يدويًا بالفعل ،
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
| useBuilderFormatting | Boolean | قيمة تشير إلى ما إذا كان التنسيق محددًا بتنسيق[`DocumentBuilder`](../) كتنسيق أساسي للنص المستورد من HTML. |

### ملاحظات

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML بأكمله.

متى*useBuilderFormatting* هو`خاطئة` ، [`DocumentBuilder`](../) يتم تجاهل التنسيق ويعتمد تنسيق text على تنسيق HTML الافتراضي. نتيجة لذلك ، يبدو النص كما هو معروض في المتصفحات.

متى*useBuilderFormatting* هو`حقيقي` ، تنسيق النص المدرج يعتمد على[`DocumentBuilder`](../) التنسيق ، والنص يبدو كما لو تم إدراجه مع[`Write`](../write/) .

### أمثلة

يوضح كيفية تطبيق تنسيق منشئ المستندات أثناء إدراج محتوى HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين محاذاة النص للمنشئ ، وأدخل فقرة HTML بمحاذاة محددة ، وأخرى بدونها.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// الفقرة الأولى لها محاذاة محددة. عندما يوزع InsertHtml كود HTML ،
// دائمًا ما تحل قيمة محاذاة الفقرة الموجودة في كود HTML محل قيمة منشئ المستند.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// لم يتم تحديد محاذاة الفقرة الثانية. يمكن أن يتم ملء قيمة المحاذاة الخاصة به
// بواسطة قيمة الباني اعتمادًا على العلامة التي مررناها إلى طريقة InsertHtml.
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

لإدراج سلسلة HTML في المستند. يسمح بتحديد خيارات إضافية.

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

يوضح كيفية استخدام الخيارات أثناء إدراج html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// بشكل افتراضي ، يُدرج "DocumentBuilder.InsertHtml" جزء HTML ينتهي بعنصر HTML على مستوى الكتلة ،
// عادةً ما تغلق هذا العنصر على مستوى الكتلة وتدرج فاصل فقرة.
// نتيجة لذلك ، تظهر فقرة فارغة جديدة بعد المستند المُدرج.
// إذا حددنا "HtmlInsertOptions.RemoveLastEmptyParagraph" ، فستتم إزالة تلك الفقرات الفارغة الإضافية.
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


