---
title: "منشئ Aspose::Words::Document::Document"
linktitle: "المستند"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Document::Document. ينشئ مستند Word فارغ في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/document/document/
---
## Document::Document() constructor


ينشئ مستند Word فارغ.

```cpp
Aspose::Words::Document::Document()
```

## ملاحظات


يتم جلب مستند فارغ من الموارد، وبشكل افتراضي، يبدو المستند الناتج كما لو تم إنشاؤه بواسطة [Word2007](../../../aspose.words.settings/mswordversion/). يحتوي هذا المستند الفارغ على جدول خطوط افتراضي، وأنماط افتراضية قليلة، وأنماط كامنة.

[OptimizeFor()](../../../aspose.words.settings/compatibilityoptions/optimizefor/) method can be used to optimize the document contents as well as default Aspose.Words behavior to a particular version of MS Word.

حجم ورق المستند هو Letter بشكل افتراضي. إذا أردت تغيير إعداد الصفحة، استخدم [PageSetup](../../section/get_pagesetup/).

بعد الإنشاء، يمكنك استخدام [DocumentBuilder](../../documentbuilder/) لإضافة محتوى المستند بسهولة.

## أمثلة



يعرض كيفية إنشاء مستند بسيط.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// كائنات Document الجديدة تأتي افتراضيًا مع الحد الأدنى من العقد
// المطلوبة لبدء إضافة محتوى مثل النص والأشكال: Section، Body، و Paragraph.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Body>>(System::MakeObject<Aspose::Words::Body>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc))->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```


يعرض كيفية إنشاء وتحميل المستندات.
```cpp
// هناك طريقتان لإنشاء كائن Document باستخدام Aspose.Words.
// 1 -  إنشاء مستند فارغ:
auto doc = System::MakeObject<Aspose::Words::Document>();

// كائنات Document الجديدة تأتي افتراضيًا مع الحد الأدنى من العقد
// المطلوبة لبدء إضافة محتوى مثل النص والأشكال: Section، Body، و Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  تحميل مستند موجود في نظام الملفات المحلي:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// المستندات المحملة ستحمل محتويات يمكننا الوصول إليها وتعديلها.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// بعض العمليات التي تحتاج إلى حدوثها أثناء التحميل، مثل استخدام كلمة مرور لفك تشفير مستند،
// يمكن القيام بها بتمرير كائن **LoadOptions** عند تحميل المستند.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


يوضح كيفية تنسيق مقطع نصي باستخدام خاصية الخط الخاصة به.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&) constructor


يفتح مستندًا موجودًا من تدفق. يكتشف تنسيق الملف تلقائيًا.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | المجري الذي يتم منه تحميل المستند. |
## ملاحظات


يجب أن يكون المستند مخزنًا في بداية الـStream. يجب أن يدعم الـStream وضعية عشوائية.

## أمثلة



يعرض كيفية تحميل مستند باستخدام stream.
```cpp
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Document.docx");
    auto doc = System::MakeObject<Aspose::Words::Document>(stream);

    ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());
}
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


يفتح مستندًا موجودًا من تدفق. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

```cpp
Aspose::Words::Document::Document(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | المجري الذي يتم منه تحميل المستند. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن أن تكون **null**. |
## ملاحظات


يجب أن يكون المستند مخزنًا في بداية الـStream. يجب أن يدعم الـStream وضعية عشوائية.

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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&) constructor


يفتح مستندًا موجودًا من ملف. يكتشف تنسيق الملف تلقائيًا.

```cpp
Aspose::Words::Document::Document(const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم ملف المستند لفتحه. |

## أمثلة



يعرض كيفية فتح مستند وتحويله إلى .PDF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToPdf.pdf");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


يفتح مستندًا موجودًا من ملف. يسمح بتحديد خيارات إضافية مثل كلمة مرور التشفير.

```cpp
Aspose::Words::Document::Document(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| fileName | const System::String\& | اسم ملف المستند لفتحه. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | خيارات إضافية لاستخدامها عند تحميل مستند. يمكن أن تكون **null**. |

## أمثلة



يعرض كيفية إنشاء وتحميل المستندات.
```cpp
// هناك طريقتان لإنشاء كائن Document باستخدام Aspose.Words.
// 1 -  إنشاء مستند فارغ:
auto doc = System::MakeObject<Aspose::Words::Document>();

// كائنات Document الجديدة تأتي افتراضيًا مع الحد الأدنى من العقد
// المطلوبة لبدء إضافة محتوى مثل النص والأشكال: Section، Body، و Paragraph.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// 2 -  تحميل مستند موجود في نظام الملفات المحلي:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// المستندات المحملة ستحمل محتويات يمكننا الوصول إليها وتعديلها.
ASSERT_EQ(u"Hello World!", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

// بعض العمليات التي تحتاج إلى حدوثها أثناء التحميل، مثل استخدام كلمة مرور لفك تشفير مستند،
// يمكن القيام بها بتمرير كائن **LoadOptions** عند تحميل المستند.
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword"));

ASSERT_EQ(u"Test encrypted document.", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
```


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

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream)
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Document::Document(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::Document::Document(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## انظر أيضًا

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
