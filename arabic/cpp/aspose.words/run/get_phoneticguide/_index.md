---
title: "طريقة Aspose::Words::Run::get_PhoneticGuide"
linktitle: "get_PhoneticGuide"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Run::get_PhoneticGuide. يحصل على كائن PhoneticGuide في C++."
type: docs
weight: 4500
url: /ar/cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


يحصل على كائن [PhoneticGuide](./).

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
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

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
