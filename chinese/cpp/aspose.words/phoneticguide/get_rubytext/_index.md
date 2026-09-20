---
title: "Aspose::Words::PhoneticGuide::get_RubyText 方法"
linktitle: "get_RubyText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PhoneticGuide::get_RubyText 方法。获取 C++ 中音标指南的 ruby 文本。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/phoneticguide/get_rubytext/
---
## PhoneticGuide::get_RubyText method


获取音标指南的 ruby 文本。

```cpp
System::String Aspose::Words::PhoneticGuide::get_RubyText()
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

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
