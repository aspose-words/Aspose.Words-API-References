---
title: "Aspose::Words::Run::get_PhoneticGuide 方法"
linktitle: "get_PhoneticGuide"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Run::get_PhoneticGuide 方法。获取一个 PhoneticGuide 对象（在 C++ 中）。"
type: docs
weight: 4500
url: /zh/cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


获取一个 [PhoneticGuide](./) 对象。

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
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

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
