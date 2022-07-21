---
title: Update
second_title: Aspose.Words لمراجع .NET API
description: يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل.
type: docs
weight: 140
url: /ar/net/aspose.words.fields/field/update/
---
## Update() {#update}

يقوم بالتحديث الميداني. يرمي إذا تم تحديث الحقل بالفعل.

```csharp
public void Update()
```

### أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام نوع الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقلين أثناء تمرير علامة تحدد ما إذا كان سيتم تحديثهما أثناء قيام المنشئ بإدخالهما.
// في بعض الحالات ، قد يكون تحديث الحقول مكلفًا من الناحية الحسابية ، وقد يكون تأجيل التحديث فكرة جيدة.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // سنحتاج إلى تحديث هذه الحقول باستخدام طرق التحديث يدويًا.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

يوضح كيفية تنسيق النتائج الميدانية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// استخدم منشئ المستندات لإدراج حقل يعرض نتيجة بدون أي تنسيق مطبق.
Field field = builder.InsertField("= 2 + 3");

Assert.AreEqual("= 2 + 3", field.GetFieldCode());
Assert.AreEqual("5", field.Result);

// يمكننا تطبيق تنسيق على نتيجة الحقل باستخدام خصائص الحقل.
// فيما يلي ثلاثة أنواع من التنسيقات التي يمكننا تطبيقها على نتيجة الحقل.
// 1 - التنسيق الرقمي:
FieldFormat format = field.Format;
format.NumericFormat = "$###.00";
field.Update();

Assert.AreEqual("= 2 + 3 \\# $###.00", field.GetFieldCode());
Assert.AreEqual("$  5.00", field.Result);

// 2 - تنسيق التاريخ / الوقت:
field = builder.InsertField("DATE");
format = field.Format;
format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());
Console.WriteLine($"Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

// 3 - التنسيق العام:
field = builder.InsertField("= 25 + 33");
format = field.Format;
format.GeneralFormats.Add(GeneralFormat.LowercaseRoman);
format.GeneralFormats.Add(GeneralFormat.Upper);
field.Update();

int index = 0;
using (IEnumerator<GeneralFormat> generalFormatEnumerator = format.GeneralFormats.GetEnumerator())
    while (generalFormatEnumerator.MoveNext())
        Console.WriteLine($"General format index {index++}: {generalFormatEnumerator.Current}");

Assert.AreEqual("= 25 + 33 \\* roman \\* Upper", field.GetFieldCode());
Assert.AreEqual("LVIII", field.Result);
Assert.AreEqual(2, format.GeneralFormats.Count);
Assert.AreEqual(GeneralFormat.LowercaseRoman, format.GeneralFormats[0]);

// يمكننا إزالة التنسيقات الخاصة بنا لإعادة نتيجة الحقل إلى شكله الأصلي.
format.GeneralFormats.Remove(GeneralFormat.LowercaseRoman);
format.GeneralFormats.RemoveAt(0);
Assert.AreEqual(0, format.GeneralFormats.Count);
field.Update();

Assert.AreEqual("= 25 + 33  ", field.GetFieldCode());
Assert.AreEqual("58", field.Result);
Assert.AreEqual(0, format.GeneralFormats.Count);
```

### أنظر أيضا

* class [Field](../../field)
* مساحة الاسم [Aspose.Words.Fields](../../field)
* المجسم [Aspose.Words](../../../)

---

## Update(bool) {#update_1}

يقوم بإجراء تحديث ميداني. يرمي إذا تم تحديث الحقل بالفعل.

```csharp
public void Update(bool ignoreMergeFormat)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| ignoreMergeFormat | Boolean | إذا`حقيقي` ثم يتم التخلي عن تنسيق نتيجة الحقل المباشر ، بغض النظر عن مفتاح MERGEFORMAT ، وإلا يتم إجراء التحديث العادي. |

### أمثلة

يوضح كيفية الاحتفاظ بحقول INCLUDEPICTURE أو تجاهلها عند تحميل مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldIncludePicture includePicture = (FieldIncludePicture)builder.InsertField(FieldType.FieldIncludePicture, true);
includePicture.SourceFullName = ImageDir + "Transparent background logo.png";
includePicture.Update(true);

using (MemoryStream docStream = new MemoryStream())
{
    doc.Save(docStream, new OoxmlSaveOptions(SaveFormat.Docx));

    // يمكننا تعيين علامة في كائن LoadOptions لتحديد ما إذا كان سيتم تحويل جميع حقول INCLUDEPICTURE
    // في أشكال الصور عند تحميل مستند يحتوي عليها.
    LoadOptions loadOptions = new LoadOptions
    {
        PreserveIncludePictureField = preserveIncludePictureField
    };

    doc = new Document(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        Assert.True(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));

        doc.UpdateFields();
        doc.Save(ArtifactsDir + "Field.PreserveIncludePicture.docx");
    }
    else
    {
        Assert.False(doc.Range.Fields.Any(f => f.Type == FieldType.FieldIncludePicture));
    }
}
```

### أنظر أيضا

* class [Field](../../field)
* مساحة الاسم [Aspose.Words.Fields](../../field)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
