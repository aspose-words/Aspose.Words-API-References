---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath metod"
linktitle: "get_IgnoreOfficeMath"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath metod. Hämtar eller anger ett booleskt värde som indikerar om text inuti OfficeMath/> ska ignoreras. Standardvärdet är true i C++."
type: docs
weight: 11250
url: /sv/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreofficemath/
---
## FindReplaceOptions::get_IgnoreOfficeMath method


Hämtar eller anger ett booleskt värde som indikerar om text inuti OfficeMath/> ska ignoreras. Standardvärdet är **true**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath() const
```


## Exempel



Visar hur man hittar och ersätter text inom OfficeMath.
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

## Se även

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
