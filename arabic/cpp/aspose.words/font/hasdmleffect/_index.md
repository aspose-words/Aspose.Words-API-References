---
title: "طريقة Aspose::Words::Font::HasDmlEffect"
linktitle: "HasDmlEffect"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::HasDmlEffect. يتحقق مما إذا كان تأثير نص DrawingML معين مطبقًا في C++."
type: docs
weight: 58000
url: /ar/cpp/aspose.words/font/hasdmleffect/
---
## Font::HasDmlEffect method


يتحقق مما إذا كان تأثير نص DrawingML معين مطبقًا.

```cpp
bool Aspose::Words::Font::HasDmlEffect(Aspose::Words::TextDmlEffect dmlEffectType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| dmlEffectType | Aspose::Words::TextDmlEffect | نوع تأثير نص DrawingML. |

### ReturnValue

**true** if particular DrawingML text effect is applied.

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

* Enum [TextDmlEffect](../../textdmleffect/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
