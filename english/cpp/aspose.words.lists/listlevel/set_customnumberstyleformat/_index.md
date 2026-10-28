---
title: Aspose::Words::Lists::ListLevel::set_CustomNumberStyleFormat method
linktitle: set_CustomNumberStyleFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLevel::set_CustomNumberStyleFormat method. Sets the custom number style format for this list level. For example: "a, ç, ĝ, ..." in C++.'
type: docs
weight: 23500
url: /cpp/aspose.words.lists/listlevel/set_customnumberstyleformat/
---
## ListLevel::set_CustomNumberStyleFormat method


Sets the custom number style format for this list level. For example: "a, ç, ĝ, ...".

```cpp
void Aspose::Words::Lists::ListLevel::set_CustomNumberStyleFormat(const System::String & value)
```

## Examples


Shows how to get the format for a list with the custom number style.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"List with leading zero.docx"));

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ((u"001, 002, 003, ..."), customNumberStyleFormat);

// We can get value for the specified index of the list item.
ASSERT_EQ(u"iv", ListLevel::GetEffectiveValue(4, NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", ListLevel::GetEffectiveValue(5, NumberStyle::Custom, customNumberStyleFormat));
```

Shows how to set customer number style format.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"List with leading zero.docx"));

doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"001.", paras->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"0001.", paras->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"0002.", paras->idx_get(2)->get_ListLabel()->get_LabelString());

paras->idx_get(1)->get_ListFormat()->get_ListLevel()->set_CustomNumberStyleFormat(u"001, 002, 003, ...");

doc->UpdateListLabels();

ASSERT_EQ(u"001.", paras->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"001.", paras->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"002.", paras->idx_get(2)->get_ListLabel()->get_LabelString());
```
## See Also

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
