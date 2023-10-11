---
title: FieldMergingArgsBase.FieldValue
second_title: Aspose.Words لمراجع .NET API
description: FieldMergingArgsBase ملكية. الحصول على قيمة الحقل أو تعيينها من مصدر البيانات.
type: docs
weight: 50
url: /ar/net/aspose.words.mailmerging/fieldmergingargsbase/fieldvalue/
---
## FieldMergingArgsBase.FieldValue property

الحصول على قيمة الحقل أو تعيينها من مصدر البيانات.

```csharp
public object FieldValue { get; set; }
```

### ملاحظات

تحتوي هذه الخاصية على قيمة تم تحديدها للتو من مصدر البيانات الخاص بك لهذا الحقل بواسطة محرك دمج المراسلات. يمكنك أيضًا استبدال القيمة عن طريق تعيين الخاصية.

### أمثلة

يوضح كيفية تحرير القيم التي تتلقاها MERGEFIELDs عند حدوث عملية دمج البريد.

```csharp
public void FieldFormats()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // قم بإدراج بعض MERGEFIELDs مع مفاتيح التنسيق التي ستقوم بتحرير القيم التي ستتلقاها أثناء دمج البريد.
    builder.InsertField("MERGEFIELD text_Field1 \\* Caps", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD text_Field2 \\* Upper", null);
    builder.Write(", ");
    builder.InsertField("MERGEFIELD numeric_Field1 \\# 0.0", null);

    builder.Document.MailMerge.FieldMergingCallback = new FieldValueMergingCallback();

    builder.Document.MailMerge.Execute(
        new string[] { "text_Field1", "text_Field2", "numeric_Field1" },
        new object[] { "Field 1", "Field 2", 10 });
    string t = doc.GetText().Trim();
    Assert.AreEqual("Merge Value For \"Text_Field1\": Field 1, MERGE VALUE FOR \"TEXT_FIELD2\": FIELD 2, 10000.0", doc.GetText().Trim());
}

/// <summary>
/// يقوم بتحرير القيم التي تتلقاها MERGEFIELDs أثناء دمج البريد.
/// يجب أن يحتوي اسم MERGEFIELD على بادئة حتى يصبح رد الاتصال هذا ساري المفعول على قيمته.
/// </summary>
private class FieldValueMergingCallback : IFieldMergingCallback
{
    /// <summary>
    /// يتم الاتصال به عندما يقوم دمج البريد بدمج البيانات في MERGEFIELD.
    /// </summary>
    void IFieldMergingCallback.FieldMerging(FieldMergingArgs e)
    {
        if (e.FieldName.StartsWith("text_"))
            e.FieldValue = $"Merge value for \"{e.FieldName}\": {(string)e.FieldValue}";
        else if (e.FieldName.StartsWith("numeric_"))
            e.FieldValue = (int)e.FieldValue * 1000;
    }

    void IFieldMergingCallback.ImageFieldMerging(ImageFieldMergingArgs e)
    {
        // لا تفعل شيئا.
    }
}
```

### أنظر أيضا

* class [FieldMergingArgsBase](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../fieldmergingargsbase/)
* المجسم [Aspose.Words](../../../)


