---
title: "طريقة Aspose::Words::PhoneticGuide::get_RubyText"
linktitle: "get_RubyText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::PhoneticGuide::get_RubyText. يحصل على نص الروبي للدليل الصوتي في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words/phoneticguide/get_rubytext/
---
## PhoneticGuide::get_RubyText method


يحصل على نص الروبي للدليل الصوتي.

```cpp
System::String Aspose::Words::PhoneticGuide::get_RubyText()
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
