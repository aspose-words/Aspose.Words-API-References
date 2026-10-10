---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath metodu"
linktitle: "get_IgnoreOfficeMath"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath metodu. OfficeMath içindeki metni yok sayıp saymayacağını belirten bir boolean değer alır veya ayarlar. Varsayılan değer C++'da true'dur."
type: docs
weight: 11250
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreofficemath/
---
## FindReplaceOptions::get_IgnoreOfficeMath method


OfficeMath/> içindeki metni yoksaymayı belirten bir boolean değeri alır veya ayarlar. Varsayılan değer **true**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath() const
```


## Örnekler



OfficeMath içinde metni bulma ve değiştirme nasıl yapılır gösterir.
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

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
