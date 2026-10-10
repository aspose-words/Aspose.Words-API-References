---
title: "Aspose::Words::Loading::LoadOptions::LoadOptions مُنشئ"
linktitle: "LoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Loading::LoadOptions::LoadOptions مُنشئ. يهيئ نسخة جديدة من هذه الفئة بالقيم الافتراضية في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.loading/loadoptions/loadoptions/
---
## LoadOptions::LoadOptions() constructor


ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions()
```


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
## LoadOptions::LoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


اختصار لإنشاء نسخة جديدة من هذه الفئة مع تعيين الخصائص إلى القيم المحددة.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| loadFormat | Aspose::Words::LoadFormat | تنسيق المستند الذي سيتم تحميله. |
| password | const System::String\& | كلمة المرور لفتح مستند مشفر. يمكن أن تكون **null** أو سلسلة فارغة. |
| baseUri | const System::String\& | السلسلة التي ستُستخدم لحل عناوين URI النسبية إلى مطلقة. يمكن أن تكون **null** أو سلسلة فارغة. |

## أمثلة



يعرض كيفية تحديد عنوان URI أساسي عند فتح مستند html.
```cpp
// افترض أننا نريد تحميل مستند .html يحتوي على صورة مرتبطة بعنوان URI نسبي
// في حين أن الصورة موجودة في موقع مختلف. في هذه الحالة، سنحتاج إلى تحويل عنوان URI النسبي إلى عنوان مطلق.
// يمكننا توفير عنوان URI أساسي باستخدام كائن HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(Aspose::Words::LoadFormat::Html, u"", get_ImageDir());

ASSERT_EQ(Aspose::Words::LoadFormat::Html, loadOptions->get_LoadFormat());

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing image.html", loadOptions);

// بينما كانت الصورة مكسورة في ملف .html المدخل، ساعدنا عنوان URI الأساسي المخصص في إصلاح الرابط.
auto imageShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(imageShape->get_IsImage());

// سيعرض مستند الإخراج هذه الصورة التي كانت مفقودة.
doc->Save(get_ArtifactsDir() + u"HtmlLoadOptions.BaseUri.docx");
```

## انظر أيضًا

* Enum [LoadFormat](../../../aspose.words/loadformat/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## LoadOptions::LoadOptions(const System::String\&) constructor


اختصار لإنشاء نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر.

```cpp
Aspose::Words::Loading::LoadOptions::LoadOptions(const System::String &password)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| password | const System::String\& | كلمة المرور لفتح مستند مشفر. يمكن أن تكون **null** أو سلسلة فارغة. |

## أمثلة



يوضح كيفية تحميل مستند Microsoft Word مشفر.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// تقوم Aspose.Words بإلقاء استثناء إذا حاولنا فتح مستند مشفر بدون كلمة المرور الخاصة به.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// عند تحميل مثل هذا المستند، يتم تمرير كلمة المرور إلى مُنشئ المستند باستخدام كائن LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// هناك طريقتان لتحميل مستند مشفر باستخدام كائن LoadOptions.
// 1 -  تحميل المستند من نظام الملفات المحلي باستخدام اسم الملف:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  تحميل المستند من تدفق:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## انظر أيضًا

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
