---
title: "منشئ Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions"
linktitle: "HtmlLoadOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions. يهيئ نسخة جديدة من هذه الفئة بالقيم الافتراضية في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.loading/htmlloadoptions/htmlloadoptions/
---
## HtmlLoadOptions::HtmlLoadOptions() constructor


ينشئ نسخة جديدة من هذه الفئة بالقيم الافتراضية.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions()
```


## أمثلة



يظهر كيفية دعم التعليقات الشرطية أثناء تحميل مستند HTML.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// إذا كانت القيمة true، فإننا نأخذ شفرة VML في الاعتبار أثناء تحليل المستند المحمَّل.
loadOptions->set_SupportVml(supportVml);

// يحتوي هذا المستند على صورة JPEG داخل وسوم "<!--[if gte vml 1]>"،
// و صورة PNG مختلفة داخل وسوم "<![if !vml]>".
// إذا قمنا بتعيين العلامة "SupportVml" إلى "true"، فستقوم Aspose.Words بتحميل صورة JPEG.
// إذا قمنا بتعيين هذه العلامة إلى "false"، فستقوم Aspose.Words بتحميل صورة PNG فقط.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## انظر أيضًا

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) constructor


اختصار لإنشاء نسخة جديدة من هذه الفئة مع تعيين الخصائص إلى القيم المحددة.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(Aspose::Words::LoadFormat loadFormat, const System::String &password, const System::String &baseUri)
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
* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlLoadOptions::HtmlLoadOptions(const System::String\&) constructor


اختصار لإنشاء نسخة جديدة من هذه الفئة باستخدام كلمة المرور المحددة لتحميل مستند مشفر.

```cpp
Aspose::Words::Loading::HtmlLoadOptions::HtmlLoadOptions(const System::String &password)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| password | const System::String\& | كلمة المرور لفتح مستند مشفر. يمكن أن تكون **null** أو سلسلة فارغة. |

## أمثلة



يوضح كيفية تشفير مستند Html، ثم فتحه باستخدام كلمة مرور.
```cpp
// إنشاء وتوقيع مستند HTML مشفر من ملف .docx مشفر.
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_Comments(u"Comment");
signOptions->set_SignTime(System::DateTime::get_Now());
signOptions->set_DecryptionPassword(u"docPassword");

System::String inputFileName = get_MyDir() + u"Encrypted.docx";
System::String outputFileName = get_ArtifactsDir() + u"HtmlLoadOptions.EncryptedHtml.html";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);

// لتحميل وقراءة هذا المستند، سنحتاج إلى تمرير فك تشفيره
// كلمة المرور باستخدام كائن HtmlLoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>(u"docPassword");

ASSERT_EQ(signOptions->get_DecryptionPassword(), loadOptions->get_Password());

auto doc = System::MakeObject<Aspose::Words::Document>(outputFileName, loadOptions);

ASSERT_EQ(u"Test encrypted document.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
