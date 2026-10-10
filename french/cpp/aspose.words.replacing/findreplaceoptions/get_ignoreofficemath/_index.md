---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath method"
linktitle: "get_IgnoreOfficeMath"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath method. Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur de OfficeMath/>. La valeur par défaut est true en C++."
type: docs
weight: 11250
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreofficemath/
---
## FindReplaceOptions::get_IgnoreOfficeMath method


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le texte à l'intérieur d'OfficeMath/>. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath() const
```


## Exemples



Montre comment rechercher et remplacer du texte dans OfficeMath.
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

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
