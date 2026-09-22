---
title: "Aspose::Words::PhoneticGuide::get_BaseText yöntemi"
linktitle: "get_BaseText"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PhoneticGuide::get_BaseText yöntemi. C++'da fonetik rehberin temel metnini alır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/phoneticguide/get_basetext/
---
## PhoneticGuide::get_BaseText method


Fonetik kılavuzun temel metnini alır.

```cpp
System::String Aspose::Words::PhoneticGuide::get_BaseText()
```


## Örnekler



Fonetik kılavuzun özelliklerini nasıl alacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// Asya metninde fonetik kılavuzu kullanın.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## Ayrıca Bakınız

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
