---
title: Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat method
linktitle: get_CustomNumberStyleFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat method. Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ..." in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.lists/listlevel/get_customnumberstyleformat/
---
## ListLevel::get_CustomNumberStyleFormat method


Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ...".

```cpp
System::String Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat()
```


## Examples



Shows how to get the format for a list with the custom number style. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// We can get value for the specified index of the list item.
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```


Shows how to set customer number style format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

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
