---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath 方法"
linktitle: "get_IgnoreOfficeMath"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath 方法。获取或设置一个布尔值，指示是否忽略 OfficeMath 中的文本。默认值在 C++ 中为 true。"
type: docs
weight: 11250
url: /zh/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreofficemath/
---
## FindReplaceOptions::get_IgnoreOfficeMath method


获取或设置一个布尔值，指示是否忽略 OfficeMath/> 中的文本。默认值为 **true**。

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath() const
```


## 示例



展示如何在 OfficeMath 中查找和替换文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

ASSERT_EQ(u"i+b-c≥iM+bM-cM", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreOfficeMath(isIgnoreOfficeMath);
doc->get_Range()->Replace(u"b", u"x", options);

if (isIgnoreOfficeMath)
{
    ASSERT_EQ(u"i+b-c≥iM+bM-cM", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
}
else
{
    ASSERT_EQ(u"i+x-c≥iM+xM-cM", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetText().Trim());
}
```

## 另见

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
