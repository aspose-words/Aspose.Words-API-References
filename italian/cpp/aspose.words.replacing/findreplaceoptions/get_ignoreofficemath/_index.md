---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath metodo"
linktitle: "get_IgnoreOfficeMath"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath metodo. Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>. Il valore predefinito è true in C++."
type: docs
weight: 11250
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreofficemath/
---
## FindReplaceOptions::get_IgnoreOfficeMath method


Ottiene o imposta un valore booleano che indica se ignorare il testo all'interno di OfficeMath/>. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath() const
```


## Esempi



Mostra come trovare e sostituire il testo all'interno di OfficeMath.
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

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
