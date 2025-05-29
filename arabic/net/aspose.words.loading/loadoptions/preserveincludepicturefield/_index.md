---
title: LoadOptions.PreserveIncludePictureField
linktitle: PreserveIncludePictureField
articleTitle: PreserveIncludePictureField
second_title: Aspose.Words لـ .NET
description: تحكم في حقل INCLUDEPICTURE بتنسيقات Microsoft Word باستخدام LoadOptions PreserveIncludePictureField. أدر تنسيق المستندات بسهولة لتحقيق أفضل النتائج.
type: docs
weight: 120
url: /ar/net/aspose.words.loading/loadoptions/preserveincludepicturefield/
---
## LoadOptions.PreserveIncludePictureField property

يحصل على أو يعين ما إذا كان سيتم الاحتفاظ بحقل INCLUDEPICTURE عند قراءة تنسيقات Microsoft Word. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool PreserveIncludePictureField { get; set; }
```

## ملاحظات

افتراضيًا، يتم تحويل حقل INCLUDEPICTURE إلى كائن شكل. يمكنك تجاوز ذلك إذا كنت بحاجة إلى حفظ الحقل باستخدام ، على سبيل المثال، إذا كنت ترغب في تحديثه برمجيًا. مع ذلك، تجدر الإشارة إلى أن هذا النهج ليس شائعًا في Aspose.Words. استخدمه على مسؤوليتك الخاصة.

من الممكن استخدام حقل MERGEFIELD كحقل فرعي لتغيير مسار المصدر path للصورة ديناميكيًا. في هذه الحالة، يجب حفظ INCLUDEPICTURE في النموذج.

## أمثلة

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

* class [LoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
