---
title: Aspose::Words::PhoneticGuide::get_RubyText method
linktitle: get_RubyText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PhoneticGuide::get_RubyText method. Gets ruby text of the phonetic guide in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/phoneticguide/get_rubytext/
---
## PhoneticGuide::get_RubyText method


Gets ruby text of the phonetic guide.

```cpp
System::String Aspose::Words::PhoneticGuide::get_RubyText()
```


## Examples



Shows how to get properties of the phonetic guide. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// Use phonetic guide in the Asian text.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## See Also

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
