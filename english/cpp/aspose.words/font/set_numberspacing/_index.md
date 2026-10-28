---
title: Aspose::Words::Font::set_NumberSpacing method
linktitle: set_NumberSpacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_NumberSpacing method. Sets the spacing type of the numeral being displayed in C++.'
type: docs
weight: 83500
url: /cpp/aspose.words/font/set_numberspacing/
---
## Font::set_NumberSpacing method


Sets the spacing type of the numeral being displayed.

```cpp
void Aspose::Words::Font::set_NumberSpacing(Aspose::Words::NumSpacing value)
```

## Examples


Shows how to set the spacing type of the numeral.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// This effect is only supported in newer versions of MS Word.
doc->get_CompatibilityOptions()->OptimizeFor(MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
