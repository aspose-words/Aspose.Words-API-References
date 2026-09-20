---
title: "Метод Aspose::Words::PhoneticGuide::get_RubyText"
linktitle: "get_RubyText"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::PhoneticGuide::get_RubyText. Получает ruby‑текст фонетического руководства в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/phoneticguide/get_rubytext/
---
## PhoneticGuide::get_RubyText method


Получает ruby‑текст фонетического гида.

```cpp
System::String Aspose::Words::PhoneticGuide::get_RubyText()
```


## Примеры



Показывает, как получить свойства фонетического руководства.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Phonetic guide.docx");

System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();
// Используйте фонетическое руководство в азиатском тексте.
ASPOSE_ASSERT_EQ(true, runs->idx_get(0)->get_IsPhoneticGuide());
ASSERT_EQ(u"base", runs->idx_get(0)->get_PhoneticGuide()->get_BaseText());
ASSERT_EQ(u"ruby", runs->idx_get(0)->get_PhoneticGuide()->get_RubyText());
```

## См. также

* Class [PhoneticGuide](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
