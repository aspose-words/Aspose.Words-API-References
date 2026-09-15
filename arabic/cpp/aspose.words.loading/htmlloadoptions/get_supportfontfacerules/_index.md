---
title: "طريقة Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules"
linktitle: "get_SupportFontFaceRules"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules. يحصل على أو يضبط قيمة تشير إلى ما إذا كان يجب دعم قواعد @font-face وما إذا كان يجب تحميل الخطوط المعلنة. القيمة الافتراضية هي false في C++."
type: docs
weight: 6500
url: /ar/cpp/aspose.words.loading/htmlloadoptions/get_supportfontfacerules/
---
## HtmlLoadOptions::get_SupportFontFaceRules method


يحصل أو يعيّن قيمة تشير إلى ما إذا كان يجب دعم قواعد @font-face وما إذا كان يجب تحميل الخطوط المعلنة. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules() const
```

## ملاحظات


إذا تم تمكين هذا الخيار، يتم تحميل الخطوط المعلنة في قواعد @font-face وتضمينها في تعريفات خطوط المستند الناتج (انظر [FontInfos](../../../aspose.words/documentbase/get_fontinfos/)). يجعل هذا الخطوط المحملة متاحة للعرض ولكن لا يفعّل تلقائيًا تضمين الخطوط عند الحفظ. لكي يتم حفظ المستند مع الخطوط المحملة، يجب ضبط خاصية [EmbedTrueTypeFonts](../../../aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/) في مجموعة [FontInfos](../../../aspose.words/documentbase/get_fontinfos/) إلى **true**.

تنسيقات الخطوط المدعومة هي TTF و EOT و WOFF.

قواعد @font-face غير مدعومة عند تحميل صور SVG.

## أمثلة



يوضح كيفية تحميل القواعد المعلنة "@font-face".
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_SupportFontFaceRules(true);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Html with FontFace.html", loadOptions);

ASSERT_EQ(u"Squarish Sans CT Regular", doc->get_FontInfos()->idx_get(0)->get_Name());
```

## انظر أيضًا

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
