---
title: Aspose::Words::NumSpacing enum
linktitle: NumSpacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NumSpacing enum. Specifies possible values in which numeral spacing can be displayed in C++.'
type: docs
weight: 103500
url: /cpp/aspose.words/numspacing/
---
## NumSpacing enum


Specifies possible values in which numeral spacing can be displayed.

```cpp
enum class NumSpacing
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Default | 0 | Specifies that numerals are displayed in the font’s default form. |
| Proportional | 1 | Specifies that the forms of the numerals designed as proportionally spaced are displayed if supported by the font. |
| Tabular | 2 | Specifies that the forms of the numerals designed as tabular are displayed if supported by the font. |


## Examples



Shows how to set the spacing type of the numeral. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// This effect is only supported in newer versions of MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
