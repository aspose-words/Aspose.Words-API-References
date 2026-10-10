---
title: "Aspose::Words::Run::get_IsPhoneticGuide metod"
linktitle: "get_IsPhoneticGuide"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Run::get_IsPhoneticGuide metod. Hämtar ett booleskt värde som indikerar om runen är en fonetisk guide i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words/run/get_isphoneticguide/
---
## Run::get_IsPhoneticGuide method


Hämtar ett booleskt värde som indikerar om körningen är en fonetisk guide.

```cpp
bool Aspose::Words::Run::get_IsPhoneticGuide()
```


## Exempel



Visar hur man får egenskaperna för den fonetiska guiden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// Använd fonetisk guide i den asiatiska texten.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## Se även

* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
