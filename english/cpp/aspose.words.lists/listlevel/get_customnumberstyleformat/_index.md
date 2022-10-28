---
title: get_CustomNumberStyleFormat
second_title: Aspose.Words for C++ API Reference
description: 'Gets the custom number style format for this list level. For example: "a, ç, ĝ, ...".'
type: docs
weight: 53
url: /cpp/aspose.words.lists/listlevel/get_customnumberstyleformat/
---
## ListLevel.get_CustomNumberStyleFormat method


Gets the custom number style format for this list level. For example: "a, ç, ĝ, ...".

```cpp
System::String Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat()
```


## Examples




Shows how to get the format for a list with the custom number style. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"List with leading zero.docx");

SharedPtr<ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

String customNumberStyleFormat = String::Empty;

if (listLevel->get_NumberStyle() == NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// We can get value for the specified index of the list item.
ASSERT_EQ(u"iv", ListLevel::GetEffectiveValue(4, NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", ListLevel::GetEffectiveValue(5, NumberStyle::Custom, customNumberStyleFormat));
```

