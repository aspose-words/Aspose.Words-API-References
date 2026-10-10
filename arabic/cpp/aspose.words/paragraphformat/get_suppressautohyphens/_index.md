---
title: "طريقة Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens"
linktitle: "get_SuppressAutoHyphens"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens طريقة. يحدد ما إذا كان الفقرة الحالية يجب أن تُعفى من أي تجزئة كلمات تُطبق في إعدادات المستند في C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


يحدد ما إذا كان يجب استثناء الفقرة الحالية من أي تجزئة تُطبق في إعدادات المستند.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## أمثلة



يعرض كيفية تعطيل تجزئة الكلمات لفقرة.
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// افتح مستندًا يحتوي على نص بتهيئة محلية تتطابق مع قاموسنا.
// عند حفظ هذا المستند بتنسيق حفظ صفحة ثابتة، سيحتوي نصه على تجزئة كلمات.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// يمكننا تعيين الخاصية "SuppressAutoHyphens" إلى "true" لتعطيل التجزئة.
// لفقرة محددة مع إبقائها مفعلة لبقية المستند.
// القيمة الافتراضية لهذه الخاصية هي "false",
// مما يعني أن كل فقرة تستخدم التجزئة افتراضيًا إذا كانت متاحة.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
