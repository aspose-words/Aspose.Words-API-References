---
title: DocumentBuilder.InsertHtml
linktitle: InsertHtml
articleTitle: InsertHtml
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك بسهولة باستخدام طريقة InsertHtml في DocumentBuilder—قم بإدراج سلاسل HTML بسلاسة لتحقيق التكامل الديناميكي للمحتوى.
type: docs
weight: 380
url: /ar/net/aspose.words/documentbuilder/inserthtml/
---
## InsertHtml(*string*) {#inserthtml}

يقوم بإدراج سلسلة HTML في المستند.

```csharp
public void InsertHtml(string html)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| html | String | سلسلة HTML لإدراجها في المستند. |

## ملاحظات

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML بأكمله.

## أمثلة

يوضح كيفية استخدام منشئ المستندات لإدراج محتوى HTML في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const string html = "<p align='right'>Paragraph right</p>" + 
                    "<b>Implicit paragraph left</b>" +
                    "<div align='center'>Div center</div>" + 
                    "<h1 align='left'>Heading 1 left.</h1>";

builder.InsertHtml(html);

// يؤدي إدراج كود HTML إلى تحليل تنسيق كل عنصر إلى تنسيق نص المستند المكافئ.
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

يوضح كيفية تنفيذ دمج البريد باستخدام معاودة الاتصال المخصصة التي تتعامل مع بيانات الدمج في شكل مستندات HTML.

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
/// تقوم وظيفة الارتداد هذه بتحليل بيانات الدمج الخاصة بها كمحتوى HTML وتضيف النتيجة إلى موقع المستند الخاص بـ MERGEFIELD.
/// </summary>
private class HandleMergeFieldInsertHtml : IFieldMergingCallback
{
    /// <summary>
    /// يتم استدعاؤها عندما يقوم دمج البريد بدمج البيانات في MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs args)
    {
        if (args.DocumentFieldName.StartsWith("html_") && args.Field.GetFieldCode().Contains("\\b"))
        {
            // أضف بيانات HTML المحللة إلى نص المستند.
            DocumentBuilder builder = new DocumentBuilder(args.Document);
            builder.MoveToMergeField(args.DocumentFieldName);
            builder.InsertHtml((string)args.FieldValue);

            // نظرًا لأننا قمنا بالفعل بإدراج المحتوى المدمج يدويًا،
            // لن نحتاج إلى الاستجابة لهذا الحدث عن طريق إرجاع المحتوى عبر خاصية "النص".
            args.Text = string.Empty;
        }
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs args)
    {
        //لا تفعل شيئا.
    }
}
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertHtml(*string, bool*) {#inserthtml_2}

يقوم بإدراج سلسلة HTML في المستند.

```csharp
public void InsertHtml(string html, bool useBuilderFormatting)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| html | String | سلسلة HTML لإدراجها في المستند. |
| useBuilderFormatting | Boolean | قيمة تشير إلى ما إذا كان التنسيق المحدد في[`DocumentBuilder`](../) يتم استخدام كتنسيق أساسي للنص المستورد من HTML. |

## ملاحظات

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML بأكمله.

عندما*useBuilderFormatting* يكون`خطأ شنيع` ، [`DocumentBuilder`](../) تم تجاهل التنسيق، ويعتمد تنسيق text المُدرج على تنسيق HTML الافتراضي. ونتيجةً لذلك، يبدو النص كما هو مُعرَّف في المتصفحات.

عندما*useBuilderFormatting* يكون`حقيقي` يعتمد تنسيق للنص المدرج على[`DocumentBuilder`](../) التنسيق، ويبدو النص كما لو تم إدراجه باستخدام[`Write`](../write/) .

## أمثلة

يوضح كيفية تطبيق تنسيق منشئ المستندات أثناء إدراج محتوى HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعيين محاذاة النص للمنشئ، وإدراج فقرة HTML بمحاذاة محددة، وأخرى بدون محاذاة.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Distributed;
builder.InsertHtml(
    "<p align='right'>Paragraph 1.</p>" +
    "<p>Paragraph 2.</p>", useBuilderFormatting);

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

// تم تحديد محاذاة الفقرة الأولى. عند تحليل InsertHtml لشيفرة HTML،
// قيمة محاذاة الفقرة الموجودة في كود HTML تحل دائمًا محل قيمة منشئ المستند.
Assert.AreEqual("Paragraph 1.", paragraphs[0].GetText().Trim());
Assert.AreEqual(ParagraphAlignment.Right, paragraphs[0].ParagraphFormat.Alignment);

// الفقرة الثانية ليس لها محاذاة محددة. يمكن ملء قيمة محاذاة الفقرة الثانية.
// حسب قيمة المنشئ اعتمادًا على العلم الذي مررناه إلى طريقة InsertHtml.
Assert.AreEqual("Paragraph 2.", paragraphs[1].GetText().Trim());
Assert.AreEqual(useBuilderFormatting ? ParagraphAlignment.Distributed : ParagraphAlignment.Left,
    paragraphs[1].ParagraphFormat.Alignment);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertHtmlWithFormatting.docx");
```

### أنظر أيضا

* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)

---

## InsertHtml(*string, [HtmlInsertOptions](../../htmlinsertoptions/)*) {#inserthtml_1}

يُدرج سلسلة HTML في المستند. يسمح بتحديد خيارات إضافية.

```csharp
public void InsertHtml(string html, HtmlInsertOptions options)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| html | String | سلسلة HTML لإدراجها في المستند. |
| options | HtmlInsertOptions | الخيارات المستخدمة عند إدراج سلسلة HTML. |

## ملاحظات

يمكنك استخدام هذه الطريقة لإدراج جزء HTML أو مستند HTML بأكمله.

## أمثلة

يوضح كيفية استخدام الخيارات أثناء إدراج HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD Name ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD EMAIL ");
builder.InsertParagraph();

// بشكل افتراضي، يقوم "DocumentBuilder.InsertHtml" بإدراج جزء HTML ينتهي بعنصر HTML على مستوى الكتلة،
// عادةً ما يقوم بإغلاق عنصر مستوى الكتلة هذا وإدراج فاصل فقرة.
// ونتيجة لذلك، تظهر فقرة فارغة جديدة بعد إدراج المستند.
// إذا قمنا بتحديد "HtmlInsertOptions.RemoveLastEmptyParagraph"، سيتم إزالة تلك الفقرات الفارغة الإضافية.
builder.MoveToMergeField("NAME");
builder.InsertHtml("<p>John Smith</p>", HtmlInsertOptions.UseBuilderFormatting | HtmlInsertOptions.RemoveLastEmptyParagraph);
builder.MoveToMergeField("EMAIL");
builder.InsertHtml("<p>jsmith@example.com</p>", HtmlInsertOptions.UseBuilderFormatting);

doc.Save(ArtifactsDir + "MailMerge.RemoveLastEmptyParagraph.docx");
```

### أنظر أيضا

* enum [HtmlInsertOptions](../../htmlinsertoptions/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
