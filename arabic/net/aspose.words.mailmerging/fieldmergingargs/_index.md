---
title: FieldMergingArgs Class
linktitle: FieldMergingArgs
articleTitle: FieldMergingArgs
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.MailMerging.FieldMergingArgs للتعامل بسلاسة مع البيانات في أحداث MergeField، مما يعزز تجربة معالجة المستندات لديك.
type: docs
weight: 4460
url: /ar/net/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class

يوفر بيانات لـ**حقل الدمج** الحدث.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class FieldMergingArgs : FieldMergingArgsBase
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | يعيد[`Document`](../fieldmergingargsbase/document/)الكائن الذي يتم تنفيذ عملية دمج البريد له. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | يحصل على اسم حقل الدمج كما هو محدد في المستند. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | يحصل على الكائن الذي يمثل حقل الدمج الحالي. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | يحصل على اسم حقل الدمج في مصدر البيانات. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | يحصل على قيمة الحقل من مصدر البيانات أو يعينها. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | يحصل على الفهرس الصفري للسجل الذي يتم دمجه. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | يحصل على اسم جدول البيانات لعملية الدمج الحالية أو سلسلة فارغة إذا لم يكن الاسم متاحًا. |
| [Text](../../aspose.words.mailmerging/fieldmergingargs/text/) { get; set; } | يحصل على النص الذي سيتم إدراجه في المستند لحقل الدمج الحالي أو يعينه. |

## ملاحظات

ال**حقل الدمج** يحدث هذا الحدث أثناء دمج البريد عند مواجهة حقل دمج بريد بسيط (x000d_) في المستند. يمكنك الاستجابة لهذا الحدث بإرجاع النص (x000d_) ليُدرجه محرك دمج البريد في المستند.

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)
