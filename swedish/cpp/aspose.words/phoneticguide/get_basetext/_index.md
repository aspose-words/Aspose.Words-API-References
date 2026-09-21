---
title: "Aspose::Words::PhoneticGuide::get_BaseText metod"
linktitle: "get_BaseText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PhoneticGuide::get_BaseText metod. Hämtar bastexten för den fonetiska guiden i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/phoneticguide/get_basetext/
---
## PhoneticGuide::get_BaseText method


Hämtar grundtexten för den fonetiska guiden.

```cpp
System::String Aspose::Words::PhoneticGuide::get_BaseText()
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

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
