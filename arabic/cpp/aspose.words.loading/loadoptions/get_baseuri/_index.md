---
title: "طريقة Aspose::Words::Loading::LoadOptions::get_BaseUri"
linktitle: "get_BaseUri"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LoadOptions::get_BaseUri. يحصل أو يحدد السلسلة التي ستُستخدم لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. يمكن أن تكون فارغة أو سلسلة فارغة. القيمة الافتراضية هي null في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.loading/loadoptions/get_baseuri/
---
## LoadOptions::get_BaseUri method


يحصل أو يعيّن السلسلة التي سيتم استخدامها لحل عناوين URI النسبية الموجودة في المستند إلى عناوين URI مطلقة عند الحاجة. يمكن أن تكون **null** أو سلسلة فارغة. القيمة الافتراضية هي **null**.

```cpp
System::String Aspose::Words::Loading::LoadOptions::get_BaseUri() const
```

## ملاحظات


تُستخدم هذه الخاصية لحل عناوين URI النسبية إلى مطلقة في الحالات التالية:

1. عند تحميل مستند HTML من تدفق ويحتوي المستند على صور بعناوين URI نسبية ولا يحتوي على عنوان URI أساسي محدد في عنصر BASE في HTML.
1. عند حفظ المستند إلى PDF وصيغ أخرى، لاسترجاع الصور المرتبطة باستخدام عناوين URI نسبية حتى يمكن حفظ الصور في المستند الناتج.



## أمثلة



يوضح كيفية فتح مستند HTML يحتوي على صور من تدفق باستخدام عنوان URI أساسي.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.html");
    // مرّر عنوان URI للمجلد الأساسي أثناء تحميله
    // بحيث يمكن العثور على أي صور بعناوين URI نسبية في مستند HTML.
    auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
    loadOptions->set_BaseUri(get_ImageDir());

    auto doc = System::MakeObject<Aspose::Words::Document>(stream, loadOptions);

    // تحقق من أن الشكل الأول في المستند يحتوي على صورة صالحة.
    auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

    ASSERT_TRUE(shape->get_IsImage());
    ASSERT_FALSE(System::TestTools::IsNull(shape->get_ImageData()->get_ImageBytes()));
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Width()), 0.01);
    ASSERT_NEAR(32.0, Aspose::Words::ConvertUtil::PointToPixel(shape->get_Height()), 0.01);
}
```

## انظر أيضًا

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
