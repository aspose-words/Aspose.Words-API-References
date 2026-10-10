---
title: "طريقة Aspose::Words::Fields::Field::get_IsDirty"
linktitle: "get_IsDirty"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fields::Field::get_IsDirty. تحصل أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى أُجريت على المستند في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.fields/field/get_isdirty/
---
## Field::get_IsDirty method


يحصل أو يعيّن ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي أُجريت على المستند.

```cpp
bool Aspose::Words::Fields::Field::get_IsDirty()
```


## أمثلة



يظهر كيفية استخدام الخاصية الخاصة لتحديث نتيجة الحقل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// اعطِ قيمة الخاصية المدمجة "Author" للمستند، ثم اعرضها باستخدام حقل.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldAuthor, true));

ASSERT_FALSE(field->get_IsDirty());
ASSERT_EQ(u"John Doe", field->get_Result());

// قم بتحديث الخاصية. لا يزال الحقل يعرض القيمة القديمة.
doc->get_BuiltInDocumentProperties()->set_Author(u"John & Jane Doe");

ASSERT_EQ(u"John Doe", field->get_Result());

// نظرًا لأن قيمة الحقل قديمة، يمكننا وضع علامة "dirty" عليها.
// ستظل هذه القيمة غير محدثة حتى نقوم بتحديث الحقل يدويًا باستخدام طريقة Field.Update().
field->set_IsDirty(true);

{
    auto docStream = System::MakeObject<System::IO::MemoryStream>();
    // إذا حفظنا دون استدعاء طريقة تحديث،
    // سيستمر الحقل في عرض القيمة غير المحدثة في المستند الناتج.
    doc->Save(docStream, Aspose::Words::SaveFormat::Docx);

    // كائن LoadOptions يحتوي على خيار لتحديث جميع الحقول
    // المعلمة بـ "dirty" عند تحميل المستند.
    auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    options->set_UpdateDirtyFields(updateDirtyFields);
    doc = System::MakeObject<Aspose::Words::Document>(docStream, options);

    ASSERT_EQ(u"John & Jane Doe", doc->get_BuiltInDocumentProperties()->get_Author());

    field = System::ExplicitCast<Aspose::Words::Fields::FieldAuthor>(doc->get_Range()->get_Fields()->idx_get(0));

    // تحديث الحقول المتسخة بهذه الطريقة يضبط تلقائيًا علم "IsDirty" الخاص بها إلى false.
    if (updateDirtyFields)
    {
        ASSERT_EQ(u"John & Jane Doe", field->get_Result());
        ASSERT_FALSE(field->get_IsDirty());
    }
    else
    {
        ASSERT_EQ(u"John Doe", field->get_Result());
        ASSERT_TRUE(field->get_IsDirty());
    }
}
```

## انظر أيضًا

* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
