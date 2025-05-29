---
title: FieldMergingArgs.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words لـ .NET
description: أدر حقول دمج مستندك بسهولة باستخدام FieldMergingArgs. اضبط أو استرجاع النص بسهولة لضمان تكامل سلس للمستندات.
type: docs
weight: 10
url: /ar/net/aspose.words.mailmerging/fieldmergingargs/text/
---
## FieldMergingArgs.Text property

يحصل على النص الذي سيتم إدراجه في المستند لحقل الدمج الحالي أو يعينه.

```csharp
public string Text { get; set; }
```

## ملاحظات

عند استدعاء معالج الحدث الخاص بك، يتم تعيين هذه الخاصية على`باطل`.

إذا تركت النص كما هو`باطل` ، سيقوم محرك دمج البريد بإدراج[`FieldValue`](../../fieldmergingargsbase/fieldvalue/) في مكان حقل الدمج.

إذا قمت بتعيين النص إلى أي سلسلة (بما في ذلك فارغة)، فسيتم إدراج السلسلة في المستند بدلاً من حقل الدمج.

## أمثلة

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

* class [FieldMergingArgs](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
