---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath método"
linktitle: "get_IgnoreOfficeMath"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath método. Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>. El valor predeterminado es true en C++."
type: docs
weight: 11250
url: /es/cpp/aspose.words.replacing/findreplaceoptions/get_ignoreofficemath/
---
## FindReplaceOptions::get_IgnoreOfficeMath method


Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath() const
```


## Ejemplos



Muestra cómo buscar y reemplazar texto dentro de OfficeMath.
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

## Ver también

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
