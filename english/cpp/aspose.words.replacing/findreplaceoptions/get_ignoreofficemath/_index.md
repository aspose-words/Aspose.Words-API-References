---
title: Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath method
linktitle: get_IgnoreOfficeMath
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath method. Gets or sets a boolean value indicating either to ignore text inside OfficeMath/>. The default value is true in C++.'
type: docs
weight: 11250
url: /cpp/aspose.words.replacing/findreplaceoptions/get_ignoreofficemath/
---
## FindReplaceOptions::get_IgnoreOfficeMath method


Gets or sets a boolean value indicating either to ignore text inside OfficeMath/>. The default value is **true**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath() const
```


## Examples



Shows how to find and replace text within OfficeMath. 
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

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
