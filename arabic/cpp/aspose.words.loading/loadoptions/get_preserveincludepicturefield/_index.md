---
title: "طريقة Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField"
linktitle: "get_PreserveIncludePictureField"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField. يحصل أو يحدد ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. القيمة الافتراضية هي false في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.loading/loadoptions/get_preserveincludepicturefield/
---
## LoadOptions::get_PreserveIncludePictureField method


يحصل أو يعيّن ما إذا كان يجب الحفاظ على حقل INCLUDEPICTURE عند قراءة صيغ Microsoft Word. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField() const
```

## ملاحظات


بشكل افتراضي، يتم تحويل حقل INCLUDEPICTURE إلى كائن شكل. يمكنك تجاوز ذلك إذا كنت بحاجة إلى الحفاظ على الحقل، على سبيل المثال، إذا رغبت في تحديثه برمجيًا. لاحظ مع ذلك أن هذا النهج غير شائع في Aspose.Words. استخدمه على مسؤوليتك الخاصة.

أحد حالات الاستخدام الممكنة قد يكون استخدام MERGEFIELD كحقل فرعي لتغيير مسار مصدر الصورة ديناميكيًا. في هذه الحالة تحتاج إلى الحفاظ على INCLUDEPICTURE في النموذج.

## أمثلة



يوضح كيفية الحفاظ على حقول INCLUDEPICTURE أو تجاهلها عند تحميل مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto includePicture = System::ExplicitCast<Aspose::Words::Fields::FieldIncludePicture>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldIncludePicture, true));
includePicture->set_SourceFullName(get_ImageDir() + u"Transparent background logo.png");
includePicture->Update(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    doc->Save(docStream, System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx));

    // يمكننا تعيين علامة في كائن LoadOptions لتحديد ما إذا كان سيتم تحويل جميع حقول INCLUDEPICTURE
    // إلى أشكال صورة عند تحميل مستند يحتوي عليها.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_PreserveIncludePictureField(preserveIncludePictureField);

    doc = System::MakeObject<Aspose::Words::Document>(docStream, loadOptions);

    if (preserveIncludePictureField)
    {
        ASSERT_TRUE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == Aspose::Words::Fields::FieldType::FieldIncludePicture;
        }))));

        doc->UpdateFields();
        doc->Save(get_ArtifactsDir() + u"Field.PreserveIncludePicture.docx");
    }
    else
    {
        ASSERT_FALSE(doc->get_Range()->get_Fields()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Fields::Field>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Fields::Field> f)>>([](System::SharedPtr<Aspose::Words::Fields::Field> f) -> bool
        {
            return f->get_Type() == Aspose::Words::Fields::FieldType::FieldIncludePicture;
        }))));
    }
}
```

## انظر أيضًا

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
