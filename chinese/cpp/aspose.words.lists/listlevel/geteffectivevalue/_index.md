---
title: "Aspose::Words::Lists::ListLevel::GetEffectiveValue 方法"
linktitle: "GetEffectiveValue"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Lists::ListLevel::GetEffectiveValue 方法。报告指定列表项索引的 ListLevel 对象的字符串表示形式。参数指定 NumberStyle，以及在 C++ 中指定 Custom 时使用的可选格式字符串。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel::GetEffectiveValue method


报告 [ListLevel](../) 对象在指定列表项索引处的字符串表示形式。参数指定 [NumberStyle](../../../aspose.words/numberstyle/)，以及在指定 [Custom](../../../aspose.words/numberstyle/) 时使用的可选格式字符串。

```cpp
static System::String Aspose::Words::Lists::ListLevel::GetEffectiveValue(int32_t index, Aspose::Words::NumberStyle numberStyle, const System::String &customNumberStyleFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| index | int32_t | 列表项的索引（必须在 1 到 32767 的范围内）。 |
| numberStyle | Aspose::Words::NumberStyle | 该 [NumberStyle](../../../aspose.words/numberstyle/) 的 [ListLevel](../) 对象。 |
| customNumberStyleFormat | const System::String\& | 当指定 [Custom](../../../aspose.words/numberstyle/) 时使用的可选格式字符串（例如 \"a, ç, ĝ, ...\"）。在其他情况下，此参数必须为 **null** 或为空。 |

### ReturnValue

在由 *index* 参数确定的位置的列表项中，使用 *numberStyle* 参数和 *customNumberStyleFormat* 参数描述的 [ListLevel](../) 对象的字符串表示形式。

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

## 另见

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [ListLevel](../)
* Namespace [Aspose::Words::Lists](../../)
* Library [Aspose.Words for C++](../../../)
