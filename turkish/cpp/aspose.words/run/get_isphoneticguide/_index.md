---
title: "Aspose::Words::Run::get_IsPhoneticGuide yöntemi"
linktitle: "get_IsPhoneticGuide"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Run::get_IsPhoneticGuide yöntemi. Run'un C++'ta fonetik bir kılavuz olup olmadığını gösteren bir boolean değer alır."
type: docs
weight: 3500
url: /tr/cpp/aspose.words/run/get_isphoneticguide/
---
## Run::get_IsPhoneticGuide method


Koşunun fonetik bir kılavuz olup olmadığını gösteren bir boolean değer döndürür.

```cpp
bool Aspose::Words::Run::get_IsPhoneticGuide()
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

* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
