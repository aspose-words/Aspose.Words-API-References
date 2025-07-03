---
title: Aspose::Words::Run::get_PhoneticGuide method
linktitle: get_PhoneticGuide
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Run::get_PhoneticGuide method. Gets a PhoneticGuide object in C++.'
type: docs
weight: 4500
url: /cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


Gets a [PhoneticGuide](./) object.

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
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

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
