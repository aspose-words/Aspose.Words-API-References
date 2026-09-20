---
title: "Метод Aspose::Words::Run::get_PhoneticGuide"
linktitle: "get_PhoneticGuide"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Run::get_PhoneticGuide. Получает объект PhoneticGuide в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words/run/get_phoneticguide/
---
## Run::get_PhoneticGuide method


Получает объект [PhoneticGuide](./).

```cpp
System::SharedPtr<Aspose::Words::PhoneticGuide> Aspose::Words::Run::get_PhoneticGuide()
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

* Class [PhoneticGuide](../../phoneticguide/)
* Class [Run](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
