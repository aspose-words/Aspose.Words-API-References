---
title: "Aspose::Words::Run::get_PhoneticGuide yöntemi"
linktitle: "get_PhoneticGuide"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Run::get_PhoneticGuide yöntemi. C++'ta bir PhoneticGuide nesnesi alır."
type: docs
weight: 4500
url: /tr/cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


Bir [PhoneticGuide](./) nesnesi alır.

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
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

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
