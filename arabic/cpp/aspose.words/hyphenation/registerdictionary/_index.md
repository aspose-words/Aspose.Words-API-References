---
title: "طريقة Aspose::Words::Hyphenation::RegisterDictionary"
linktitle: "RegisterDictionary"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Hyphenation::RegisterDictionary. تقوم بتسجيل وتحميل قاموس الفواصل للغة المحددة من تدفق. تُرمى استثناء إذا تعذر قراءة القاموس أو كان بتنسيق غير صالح في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


يسجل ويحمل قاموس تجزئة للغة المحددة من تدفق. يرمي استثناءً إذا تعذر قراءة القاموس أو كان تنسيقه غير صالح.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| اللغة | const System::String\& | اسم لغة، على سبيل المثال "en-US". راجع وثائق .NET للحصول على "اسم الثقافة" وRFC 4646 للتفاصيل. |
| تدفق | const System::SharedPtr\<System::IO::Stream\>\& | تدفق لملف القاموس بتنسيق OpenOffice. |

## انظر أيضًا

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


يقوم بتسجيل وتحميل قاموس الفواصل للغة المحددة من ملف. تُرمى استثناء إذا تعذر قراءة القاموس أو كان بتنسيق غير صالح. يمكن أيضًا استخدام هذه الطريقة لتسجيل قاموس Null لمنع استدعاء [Callback](../get_callback/) بشكل متكرر لنفس اللغة.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| اللغة | const System::String\& | اسم لغة، على سبيل المثال "en-US". راجع وثائق .NET للحصول على "اسم الثقافة" وRFC 4646 للتفاصيل. |
| fileName | const System::String\& | مسار إلى ملف القاموس بتنسيق Open Office. إذا كان هذا المعامل **null** أو سلسلة فارغة فسيتم تسجيل قاموس Null ولن يتم استدعاء الـ callback بعد الآن لهذه اللغة. لتمكين الـ callback مرة أخرى استخدم طريقة [UnregisterDictionary()](../). |

## أمثلة



يظهر كيفية تسجيل قاموس تجزئة.
```cpp
// يحتوي قاموس التجزئة على قائمة من السلاسل التي تحدد قواعد التجزئة للغة القاموس.
// عندما يحتوي المستند على أسطر نصية يمكن فيها تقسيم كلمة ومتابعتها في السطر التالي،
// ستبحث التجزئة في قائمة السلاسل في القاموس عن أجزاء تلك الكلمة.
// إذا كان القاموس يحتوي على جزء من السلسلة، فستقسم التجزئة الكلمة عبر سطرين
// بحسب الجزء وتضيف شرطة إلى النصف الأول.
// سجِّل ملف قاموس من نظام الملفات المحلي إلى الإعداد المحلي \"de-CH\".
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// افتح مستندًا يحتوي على نص بالإعداد المحلي المتطابق مع قاموسنا،
// واحفظه بتنسيق حفظ ثابت الصفحات. سيُجرى تجزئة النص في ذلك المستند.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// أعد تحميل المستند بعد إلغاء تسجيل القاموس،
// واحفظه إلى ملف PDF آخر، الذي لن يحتوي على نص مجزأ.
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## انظر أيضًا

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## انظر أيضًا

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
