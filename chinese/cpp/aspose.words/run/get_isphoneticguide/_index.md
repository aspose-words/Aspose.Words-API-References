---
title: "Aspose::Words::Run::get_IsPhoneticGuide 方法"
linktitle: "get_IsPhoneticGuide"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Run::get_IsPhoneticGuide 方法。获取一个布尔值，指示该运行是否为音标指南（在 C++ 中）。"
type: docs
weight: 3500
url: /zh/cpp/aspose.words/run/get_isphoneticguide/
---
## Run::get_IsPhoneticGuide method


获取一个布尔值，指示该运行是否为拼音指南。

```cpp
bool Aspose::Words::Run::get_IsPhoneticGuide()
```


## 示例



展示如何获取音标指南的属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// 在亚洲文本中使用音标指南。
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## 另见

* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
