---
title: Aspose::Words::Font::get_NumberSpacing method
linktitle: get_NumberSpacing
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_NumberSpacing method. Gets or sets the spacing type of the numeral being displayed in C++.'
type: docs
weight: 30500
url: /cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


Gets or sets the spacing type of the numeral being displayed.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


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

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
