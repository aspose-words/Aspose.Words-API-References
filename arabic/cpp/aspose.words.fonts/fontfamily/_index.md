---
title: "Aspose::Words::Fonts::FontFamily تعداد"
linktitle: "FontFamily"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontFamily تعداد. يمثل عائلة الخط في C++."
type: docs
weight: 21000
url: /ar/cpp/aspose.words.fonts/fontfamily/
---
## FontFamily enum


يمثل عائلة الخط.

```cpp
enum class FontFamily
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| تلقائي | 0 | يحدد اسم عائلة عام. يُستخدم هذا الاسم عندما لا توجد معلومات عن الخط أو لا تهم. يتم استخدام الخط الافتراضي. |
| رومان | 1 | يحدد خطًا نسبيًا مع حواف. مثال على ذلك هو Times New Roman. |
| سويس | 2 | يحدد خطًا نسبيًا بدون حواف. مثال على ذلك هو Arial. |
| حديث | 3 | يحدد خطًا أحادي العرض مع أو بدون حواف. عادةً ما تكون الخطوط أحادية العرض حديثة؛ تشمل الأمثلة Pica و Elite و Courier New. |
| سكريبت | 4 | يحدد خطًا مصممًا ليبدو كخط اليد؛ تشمل الأمثلة Script و Cursive. |
| زخرفي | 5 | يحدد خطًا ترفيهيًا. مثال على ذلك هو Old English. |

## ملاحظات


عائلة الخطوط هي مجموعة من الخطوط ذات عرض الخط وحواف مشتركة.

## أمثلة



يعرض كيفية الوصول إلى تفاصيل كل خط في المستند وطباعةها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (System::String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // عادةً ما تكون الأسماء البديلة فارغة.
        std::cout << (System::String(u"Alt name: ") + fontInfo->get_AltName()) << std::endl;
        std::cout << (System::String(u"\t- Family: ") + System::ObjectExt::ToString(fontInfo->get_Family())) << std::endl;
        std::cout << (System::String(u"\t- ") + (fontInfo->get_IsTrueType() ? System::String(u"Is TrueType") : System::String(u"Is not TrueType"))) << std::endl;
        std::cout << (System::String(u"\t- Pitch: ") + System::ObjectExt::ToString(fontInfo->get_Pitch())) << std::endl;
        std::cout << (System::String(u"\t- Charset: ") + fontInfo->get_Charset()) << std::endl;
        std::cout << "\t- Panose:" << std::endl;
        std::cout << (System::String(u"\t\tFamily Kind: ") + fontInfo->get_Panose()[0]) << std::endl;
        std::cout << (System::String(u"\t\tSerif Style: ") + fontInfo->get_Panose()[1]) << std::endl;
        std::cout << (System::String(u"\t\tWeight: ") + fontInfo->get_Panose()[2]) << std::endl;
        std::cout << (System::String(u"\t\tProportion: ") + fontInfo->get_Panose()[3]) << std::endl;
        std::cout << (System::String(u"\t\tContrast: ") + fontInfo->get_Panose()[4]) << std::endl;
        std::cout << (System::String(u"\t\tStroke Variation: ") + fontInfo->get_Panose()[5]) << std::endl;
        std::cout << (System::String(u"\t\tArm Style: ") + fontInfo->get_Panose()[6]) << std::endl;
        std::cout << (System::String(u"\t\tLetterform: ") + fontInfo->get_Panose()[7]) << std::endl;
        std::cout << (System::String(u"\t\tMidline: ") + fontInfo->get_Panose()[8]) << std::endl;
        std::cout << (System::String(u"\t\tX-Height: ") + fontInfo->get_Panose()[9]) << std::endl;
    }
}
```

## انظر أيضًا

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
