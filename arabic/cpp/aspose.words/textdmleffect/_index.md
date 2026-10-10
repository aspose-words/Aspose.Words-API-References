---
title: "تعداد Aspose::Words::TextDmlEffect"
linktitle: "TextDmlEffect"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::TextDmlEffect enum. تأثير نص Dml لتشغيلات النص في C++."
type: docs
weight: 122000
url: /ar/cpp/aspose.words/textdmleffect/
---
## TextDmlEffect enum


تأثير نص Dml لتشغيلات النص.

```cpp
enum class TextDmlEffect
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Glow | 0 | تأثير التوهج، حيث يتم إضافة حدود ملونة مشوشة خارج حواف الكائن. |
| Fill | 1 | تأثير تغطية التعبئة. |
| Shadow | 2 | تأثير الظل. |
| Outline | 3 | تأثير الحد. |
| Effect3D | 4 | تأثير ثلاثي الأبعاد. |
| Reflection | 5 | تأثير الانعكاس. |


## أمثلة



يظهر كيفية التحقق مما إذا كان تشغيل النص يعرض تأثير نص DrawingML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"DrawingML text effects.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_TRUE(runs->idx_get(0)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(1)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Shadow));
ASSERT_TRUE(runs->idx_get(2)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Reflection));
ASSERT_TRUE(runs->idx_get(3)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Effect3D));
ASSERT_TRUE(runs->idx_get(4)->get_Font()->HasDmlEffect(Aspose::Words::TextDmlEffect::Fill));
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
