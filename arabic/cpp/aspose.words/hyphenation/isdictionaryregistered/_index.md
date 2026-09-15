---
title: "Aspose::Words::Hyphenation::IsDictionaryRegistered method"
linktitle: "IsDictionaryRegistered"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Hyphenation::IsDictionaryRegistered method. تُرجع false إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان القاموس المسجل هو Null dictionary، وتُرجع true في غير ذلك في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation::IsDictionaryRegistered method


يرجع **false** إذا لم يكن هناك قاموس مسجل للغة المحددة أو إذا كان القاموس المسجل Null، **true** خلاف ذلك.

```cpp
static bool Aspose::Words::Hyphenation::IsDictionaryRegistered(const System::String &language)
```


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
