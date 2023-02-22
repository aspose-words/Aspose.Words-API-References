---
title: FieldMergingArgsBase.Field
second_title: Aspose.Words لمراجع .NET API
description: FieldMergingArgsBase ملكية. الحصول على الكائن الذي يمثل حقل الدمج الحالي.
type: docs
weight: 30
url: /ar/net/aspose.words.mailmerging/fieldmergingargsbase/field/
---
## FieldMergingArgsBase.Field property

الحصول على الكائن الذي يمثل حقل الدمج الحالي.

```csharp
public FieldMergeField Field { get; }
```

### أمثلة

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

* class [FieldMergeField](../../../aspose.words.fields/fieldmergefield/)
* class [FieldMergingArgsBase](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* المجسم [Aspose.Words](../../../)


