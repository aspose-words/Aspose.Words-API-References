---
title: "طريقة Aspose::Words::PhoneticGuide::get_BaseText"
linktitle: "get_BaseText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PhoneticGuide::get_BaseText. يحصل على النص الأساسي للدليل الصوتي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/phoneticguide/get_basetext/
---
## PhoneticGuide::get_BaseText method


يحصل على النص الأساسي للدليل الصوتي.

```cpp
System::String Aspose::Words::PhoneticGuide::get_BaseText()
```


## أمثلة



يظهر كيفية الحصول على خصائص الدليل الصوتي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// استخدم الدليل الصوتي في النص الآسيوي.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## انظر أيضًا

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
