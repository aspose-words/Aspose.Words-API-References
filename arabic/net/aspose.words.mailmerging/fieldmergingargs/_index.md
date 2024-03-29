---
title: FieldMergingArgs Class
linktitle: FieldMergingArgs
articleTitle: FieldMergingArgs
second_title: Aspose.Words لـ .NET
description: Aspose.Words.MailMerging.FieldMergingArgs فصل. يوفر بيانات لـمجال مدمج حدث في C#.
type: docs
weight: 3770
url: /ar/net/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class

يوفر بيانات لـ**مجال مدمج** حدث.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class FieldMergingArgs : FieldMergingArgsBase
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.mailmerging/fieldmergingargsbase/document/) { get; } | إرجاع[`Document`](../fieldmergingargsbase/document/) الكائن الذي يتم تنفيذ دمج البريد له. |
| [DocumentFieldName](../../aspose.words.mailmerging/fieldmergingargsbase/documentfieldname/) { get; } | يحصل على اسم حقل الدمج كما هو محدد في الوثيقة. |
| [Field](../../aspose.words.mailmerging/fieldmergingargsbase/field/) { get; } | الحصول على الكائن الذي يمثل حقل الدمج الحالي. |
| [FieldName](../../aspose.words.mailmerging/fieldmergingargsbase/fieldname/) { get; } | الحصول على اسم حقل الدمج في مصدر البيانات. |
| [FieldValue](../../aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/) { get; set; } | الحصول على قيمة الحقل أو تعيينها من مصدر البيانات. |
| [RecordIndex](../../aspose.words.mailmerging/fieldmergingargsbase/recordindex/) { get; } | الحصول على الفهرس الصفري للسجل الذي يتم دمجه. |
| [TableName](../../aspose.words.mailmerging/fieldmergingargsbase/tablename/) { get; } | يحصل على اسم جدول البيانات لعملية الدمج الحالية أو سلسلة فارغة إذا كان الاسم غير متاح. |
| [Text](../../aspose.words.mailmerging/fieldmergingargs/text/) { get; set; } | الحصول على أو تعيين النص الذي سيتم إدراجه في المستند لحقل الدمج الحالي. |

## ملاحظات

ال**مجال مدمج** يحدث هذا الحدث أثناء دمج البريد عند مواجهة حقل merge بسيط للبريد في المستند. يمكنك الرد على هذا الحدث بإرسال نص return لمحرك دمج المراسلات لإدراجه في المستند.

## أمثلة

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

* class [FieldMergingArgsBase](../fieldmergingargsbase/)
* مساحة الاسم [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../)
