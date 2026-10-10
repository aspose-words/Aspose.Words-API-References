---
title: "Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat 方法"
linktitle: "get_CustomNumberStyleFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat 方法。获取或设置此列表级别的自定义编号样式格式。例如：\\\"a, ç, ĝ, ...\\\"（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.lists/listlevel/get_customnumberstyleformat/
---
## ListLevel::get_CustomNumberStyleFormat method


获取或设置此列表级别的自定义编号样式格式。例如："a, ç, ĝ, ..."。

```cpp
System::String Aspose::Words::Lists::ListLevel::get_CustomNumberStyleFormat()
```


## 示例



展示如何获取具有自定义编号样式的列表的格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List with leading zero.docx");

System::SharedPtr<Aspose::Words::Lists::ListLevel> listLevel = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ListFormat()->get_ListLevel();

System::String customNumberStyleFormat = System::String::Empty;

if (listLevel->get_NumberStyle() == Aspose::Words::NumberStyle::Custom)
{
    customNumberStyleFormat = listLevel->get_CustomNumberStyleFormat();
}

ASSERT_EQ(u"001, 002, 003, ...", customNumberStyleFormat);

// 我们可以获取列表项指定索引的值。
ASSERT_EQ(u"iv", Aspose::Words::Lists::ListLevel::GetEffectiveValue(4, Aspose::Words::NumberStyle::LowercaseRoman, nullptr));
ASSERT_EQ(u"005", Aspose::Words::Lists::ListLevel::GetEffectiveValue(5, Aspose::Words::NumberStyle::Custom, customNumberStyleFormat));
```


展示如何设置自定义编号样式格式。
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

## 另见

* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
