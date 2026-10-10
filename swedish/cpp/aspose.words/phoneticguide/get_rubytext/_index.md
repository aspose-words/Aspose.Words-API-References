---
title: "Aspose::Words::PhoneticGuide::get_RubyText metod"
linktitle: "get_RubyText"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PhoneticGuide::get_RubyText metod. Hämtar ruby-texten för den fonetiska guiden i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/phoneticguide/get_rubytext/
---
## PhoneticGuide::get_RubyText method


Hämtar ruby-texten för den fonetiska guiden.

```cpp
System::String Aspose::Words::PhoneticGuide::get_RubyText()
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
