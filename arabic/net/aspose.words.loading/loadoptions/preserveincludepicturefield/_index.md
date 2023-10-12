---
title: LoadOptions.PreserveIncludePictureField
second_title: Aspose.Words لمراجع .NET API
description: LoadOptions ملكية. الحصول على أو تعيين ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 120
url: /ar/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

الحصول على أو تعيين ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

### ملاحظات

بشكل افتراضي، يتم تحويل الحقل INCLUDEPICTURE إلى كائن شكل. يمكنك تجاوز ذلك إذا كنت تحتاج إلى الحقل المراد الاحتفاظ به، على سبيل المثال، إذا كنت ترغب في تحديثه برمجيًا. ومع ذلك، لاحظ أن أسلوب this ليس شائعًا في Aspose.Words. استخدامه على مسؤوليتك الخاصة.

قد تكون إحدى حالات الاستخدام المحتملة هي استخدام MERGEFIELD كحقل فرعي لتغيير مسار المصدر للصورة ديناميكيًا. في هذه الحالة تحتاج إلى حفظ INCLUDEPICTURE في النموذج.

### أمثلة

يوضح كيفية الحفاظ على حقول INCLUDEPICTURE أو تجاهلها عند تحميل مستند.

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
    // إلى أشكال الصور عند تحميل مستند يحتوي عليها.
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

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../loadoptions/)
* المجسم [Aspose.Words](../../../)


